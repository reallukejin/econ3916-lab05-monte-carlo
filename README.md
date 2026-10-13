# econ3916-lab05-monte-carlo# Monte Carlo Engine -- Probability & Simulation

## Objective

I used random simulation in Python to estimate probabilities and portfolio risk that are hard to work out by hand, and checked the results against theory.

## Methodology

- Simulated 10,000 coin flips and plotted the running share of heads to see it settle toward 0.5.
- Simulated 10,000 Monty Hall games, playing each one with an "always stay" and an "always switch" strategy, and counted the wins for each.
- Simulated a disease screening test on 100,000 people with 1% prevalence, 95% sensitivity and 90% specificity, then measured what share of positive tests came from people who were actually sick.
- Drew 10,000 daily portfolio returns from a Normal distribution and used them to compute the 95% and 99% Value at Risk and Expected Shortfall for a $1M portfolio.
- Had an AI write a reusable VaR and ES function, then checked its output against my own numbers.
- Estimated pi with Monte Carlo at different sample sizes and checked that the error shrinks like 1/sqrt(n).

## Key Findings

- **Monty Hall:** Switching won [YOUR VALUE] of 10,000 games, about twice as often as staying. The host's choice gives you information because he always avoids the car.
- **Disease screening:** Only [YOUR VALUE]% of positive tests were actually sick. The disease is rare, so false positives from healthy people outnumber the true positives, even with a 95% sensitive test.
- **Portfolio risk:** On a $1M portfolio, the 95% VaR was $[YOUR VALUE] and the 95% ES was $[YOUR VALUE]. VaR is the loss exceeded on only 5% of days, not the maximum loss, and ES shows the average loss on those worst days.
- **Monte Carlo error:** The error in the pi estimate shrank like 1/sqrt(n), so getting 10 times more accuracy takes about 100 times more samples.
