#  Var-and-CVar-Risk-Modelling


VaR answers the question: What is the maximum expected loss over a given time horizon at a certain confidence level?

For example, a 1-day 95% VaR of $1 million means there is a 95% chance the portfolio will not lose more than $1 million in one day.

CVaR measures the expected loss, given that the loss has exceeded the VaR threshold. 

It provides insight into the "tail risk"—the average of the worst losses beyond the VaR cutoff.

**CVaR (or Expected Shortfall)** tells you:

> “If losses do exceed the VaR, how bad could they get on average?”


A 1-day 95% **CVaR** of $1.3 million means that **if losses exceed the 1-day 95% VaR**, the **average loss** would be **$1.3 million**.


VaR only tells you how bad things could get up to a threshold. CVaR tells you how bad it actually gets beyond that threshold—so it captures tail risk better.

--------


VaR Formula:
----
Mathematically:

<img width="410" alt="image" src="https://github.com/user-attachments/assets/d179613b-066b-4475-810c-cff2864fb8e6" />



CVaR Formula:
------
Mathematically:

<img width="410" alt="image" src="https://github.com/user-attachments/assets/2227b44c-9f56-4061-9dea-b3751f904b6a" />




-------
**Three ways to Calculate VaR and CVaR:**

**1. Historical Way:**


In the historical method, we use actual historical daily returns of a portfolio to estimate its risk.

First, we collect the daily returns of the portfolio over a period of time and place them into an array.

Next, we sort these returns in ascending order — from the largest loss (most negative return) to the largest gain (most positive return).

To calculate the Value at Risk (VaR) at a certain confidence level (for example, 95%), we select the return at the percentile corresponding to (1 - confidence level).
For a 95% confidence level, this would be the 5th percentile return. This value represents the maximum expected loss under normal conditions.

To calculate the Conditional Value at Risk (CVaR), also known as Expected Shortfall:

We take all returns that are equal to or worse than the VaR — that is, all returns that are more negative than the VaR value.

Then, we calculate the average of these worst-case losses.

This average represents the expected loss in the worst 5% (or appropriate tail) of cases, giving a more comprehensive view of tail risk than VaR alone.

--------

**2. Parametric Method (Variance-Covariance or Analytical Method)**

This method assumes that returns are normally distributed.

We estimate the mean (average return) and standard deviation (volatility) of portfolio returns.

VaR is calculated using the normal distribution's z-score corresponding to the chosen confidence level:

<img width="148" alt="image" src="https://github.com/user-attachments/assets/229575ae-6700-4cf0-80b2-ab16574f8254" />

CVaR (Expected Shortfall) under normality is computed by integrating over the tail of the normal distribution. It gives the expected loss beyond the VaR threshold.

This method is fast but relies on the strong assumption of normality, which often underestimates tail risks.

-------

**3. Monte Carlo Simulation Method**

This method involves generating a large number of simulated future return scenarios based on statistical models.

We simulate hypothetical returns using the estimated mean and standard deviation, or from more complex models (e.g., correlated assets, fat tails).

All simulated returns are stored, then sorted from worst to best.

VaR is determined by selecting the value at the (1 - confidence level) percentile of simulated returns.

CVaR is the average of all simulated losses that are worse than the VaR, providing a better picture of extreme losses.

This method is flexible and can capture non-normal behavior, but it's computationally intensive.




---------
Use Cases
-------
  Portfolio Risk Management
  
  Quantitative Strategy Evaluation
  
  Trading Risk Limits
  
  Regulatory Risk Reporting (Basel III, SEBI)
  
