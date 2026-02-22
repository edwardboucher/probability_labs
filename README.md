# US Roulette Probability Lab v2

An interactive web application for learning probability, statistics, and Python programming through the lens of American roulette.

## Overview

This single-page HTML application provides four learning modules that progressively build your understanding of probability mathematics and how to model random systems in code.

## Features

### 🎡 Spin & Observe

An animated US roulette wheel with real-time statistics tracking. Spin the wheel and watch your observed frequencies for red, black, and green converge toward their theoretical values over time. Includes a visual frequency bar chart comparing your results against expected probabilities and a scrolling spin history.

### 📐 Probability Math

Educational reference cards covering core concepts:

- **Basic probability** — P(event) = favorable outcomes / total outcomes
- **US wheel structure** — 38 pockets: 18 red, 18 black, 2 green (0 and 00)
- **House edge** — 2/38 = 5.26% on all standard bets
- **Expected value (EV)** — how to calculate average loss per bet
- **Law of Large Numbers** — why short-term variance doesn't change long-term outcomes
- **Variance and standard deviation** — measuring the spread of results
- **Gambler's Ruin** — why a finite bankroll against an infinite one always loses
- **Bet odds table** — payouts, probabilities, and house edge for every standard bet type

### 🐍 Python Code

Five copy-ready Python scripts with syntax highlighting, ordered by complexity:

1. **Basic simulation** — modeling the wheel with `random.choice()`, lists, and sets
2. **Probability calculations** — exact fractions vs empirical frequencies using the `fractions` module
3. **Expected value calculator** — computing EV and house edge for all bet types
4. **Monte Carlo visualization** — simulating hundreds of sessions and plotting bankroll paths with `matplotlib`
5. **Convergence demo** — visualizing the Law of Large Numbers as red frequency stabilizes over thousands of spins

### 📊 Monte Carlo Simulator

A configurable in-browser Monte Carlo engine. Adjust bet type, bet size, spins per session, and number of sessions, then run the simulation to see:

- Bankroll paths for all sessions plotted together
- Expected value trendline overlay
- Win rate, average P/L, best/worst outcomes, and standard deviation
- Observed vs theoretical house edge comparison
- Written analysis of results

## Probability Quick Reference

| Outcome | Pockets | Probability | Decimal |
|---------|---------|-------------|---------|
| Red     | 18 / 38 | 9/19        | 47.37%  |
| Black   | 18 / 38 | 9/19        | 47.37%  |
| Green   | 2 / 38  | 1/19        | 5.26%   |

| Bet Type              | Payout | Win Probability | House Edge |
|-----------------------|--------|-----------------|------------|
| Straight (1 number)   | 35:1   | 2.63%           | 5.26%      |
| Split (2 numbers)     | 17:1   | 5.26%           | 5.26%      |
| Street (3 numbers)    | 11:1   | 7.89%           | 5.26%      |
| Corner (4 numbers)    | 8:1    | 10.53%          | 5.26%      |
| Six Line (6 numbers)  | 5:1    | 15.79%          | 5.26%      |
| Dozen / Column        | 2:1    | 31.58%          | 5.26%      |
| Red / Black / Odd / Even | 1:1 | 47.37%          | 5.26%      |
| Top Line (0,00,1,2,3) | 6:1   | 13.16%          | 7.89%      |

## Usage

Open `roulette.html` in any modern web browser. No server, dependencies, or build step required.

## Python Scripts

The Python tab contains standalone scripts you can copy and run locally. Requirements:

- Python 3.7+
- `matplotlib` and `numpy` (for scripts 4 and 5)

Install dependencies:

```bash
pip install matplotlib numpy
```

## Key Concepts Demonstrated

- **Probability theory** — sample spaces, events, and the probability formula
- **Expected value** — weighted average of all possible outcomes
- **Law of Large Numbers** — empirical frequency converges to theoretical probability
- **Monte Carlo simulation** — using randomness to estimate probabilistic outcomes
- **Variance and standard deviation** — quantifying uncertainty and risk
- **House edge** — the mathematical basis of casino profitability
- **Python fundamentals** — random module, sets, list comprehensions, functions, f-strings, and data visualization

## License

Educational use. Built for learning probability and Python programming.