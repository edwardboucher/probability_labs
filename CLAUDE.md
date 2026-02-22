# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A single-file educational web app (`roulette.html`) for learning probability and statistics through US roulette. No build step, no dependencies, no framework — the entire application lives in one HTML file.

## Running the App

Open `roulette.html` directly in any modern browser. No server required.

## CI

Pushes and PRs to `main` trigger `.github/workflows/jekyll-docker.yml`, which runs a Jekyll build via Docker:

```bash
docker run -v $PWD:/srv/jekyll -v $PWD/_site:/srv/jekyll/_site \
  jekyll/builder:latest /bin/bash -c "chmod -R 777 /srv/jekyll && jekyll build --future"
```

## Architecture

Everything is in `roulette.html` — HTML, CSS (with CSS custom properties for theming), and JavaScript. The app is organized into four tab-based modules rendered by a client-side tab switcher:

1. **Spin & Observe** — animated roulette wheel with live frequency tracking and a bar chart
2. **Probability Math** — static reference cards (house edge, EV, LLN, variance, Gambler's Ruin, bet odds table)
3. **Python Code** — five standalone Python scripts with syntax highlighting (copy-ready)
4. **Monte Carlo Simulator** — configurable in-browser simulation engine rendering bankroll paths and summary statistics via Canvas

The Python scripts in the "Python Code" tab are embedded as text inside the HTML (not executed in the browser). Scripts 4 and 5 require `matplotlib` and `numpy` when run locally.

## Key Domain Values

- US roulette wheel: 38 pockets (18 red, 18 black, 2 green: 0 and 00)
- House edge on all standard bets: 5.26% (2/38); Top Line only: 7.89%
- P(red) = P(black) = 18/38 = 9/19 ≈ 47.37%; P(green) = 2/38 = 1/19 ≈ 5.26%
