#  Var-and-CVar-Risk-Modelling

This project provides an end-to-end implementation of Value at Risk (VaR) and Conditional Value at Risk (CVaR) for financial risk management. These are standard tools used by quantitative analysts, portfolio managers, and financial institutions to measure and control downside risk.

VaR answers the question: What is the maximum expected loss over a given time horizon at a certain confidence level?

For example: If a portfolio has a 1-day 95% VaR of ₹10 lakh, it means there’s a 5% chance of losing more than ₹10 lakh in a day.

CVaR (also called Expected Shortfall) is the expected loss given that the loss is beyond the VaR.

VaR only tells you how bad things could get up to a threshold. CVaR tells you how bad it actually gets beyond that threshold—so it captures tail risk better.

-------

VaR Formula:
----
Mathematically:

<img width="410" alt="image" src="https://github.com/user-attachments/assets/d179613b-066b-4475-810c-cff2864fb8e6" />



CVaR Formula:
------
Mathematically:

<img width="410" alt="image" src="https://github.com/user-attachments/assets/2227b44c-9f56-4061-9dea-b3751f904b6a" />



---------
Future Enhancements:
----
  Monte Carlo Simulation-based VaR/CVaR

  Multi-asset portfolio VaR with correlation matrices

  Backtesting and stress testing module

  Visualization of loss distributions


---------
Use Cases
-------
  Portfolio Risk Management
  
  Quantitative Strategy Evaluation
  
  Trading Risk Limits
  
  Regulatory Risk Reporting (Basel III, SEBI)
  
