# Kelly Bet Size Simulator

**[Open the simulator →](https://scottfreellc.github.io/kelly-simulator/)**

An interactive demonstration of what happens to the Kelly criterion when
you don't know your edge exactly.

Kelly gives the growth-optimal bet size *conditional on knowing the true
win probability*. Set the believed and true probabilities five points
apart and watch full Kelly's median portfolio lose money while its mean
reads spectacular — and watch a flat 2% stake survive scenarios that
ruin 40% of full-Kelly runs.

Four sizing rules run side by side on identical coin flips, so what you
see diverge is sizing and never luck.

## What it shows

| Control | What it does |
|---|---|
| True win probability | What actually happens. Reality never tells you this. |
| Believed win probability | What your model claims. Every rule sizes its bet on this. |
| Contract price | Costs this to buy, pays $1 if it resolves YES. |
| Bets per run | How *long* one simulated lifetime is. |
| Number of runs | How *many* independent lifetimes run at once. |

A run counts as ruined below 10% of the starting portfolio — not zero,
because a portfolio down 90% cannot practically recover, and waiting for
literal zero understates how often overbetting destroys an account.

Deterministic: the same settings always produce the same result.

## Running it

It is a single self-contained HTML file — no build step, no
dependencies, no network. Clone and open `index.html`, or just use the
hosted link above.

## Background

- Kelly, J. L. (1956), *A New Interpretation of Information Rate*
- Bailey & López de Prado (2014), *The Deflated Sharpe Ratio* — the
  companion idea that a backtest's Sharpe must be corrected for how many
  strategies were tried

## Scope

This is a simulation of a mathematical result. It is not financial
advice, it makes no claim about expected returns, and it is not a
recommendation about how to size anything. It exists to show why a
position-size cap can be far below the Kelly stake and still be the
right choice.

Built for [Prediction Markets with AI Agents](https://maven.com/scottfree/prediction-markets),
a one-day workshop on the engineering discipline behind agentic
forecasting systems.

Apache License 2.0.
