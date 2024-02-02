# Python Applications in Finance
This repository is meant for finance-related discovery projects to learn more about how Python can be used in finance and explore topics I am curious about. I do not claim any of these projects as my own as they were completed by following a YouTube tutorial. They purely serve as a hands-on introduction to applying programming in finance.

This repository contains the following projects:
1. Risk Factor Model Estimation of a Stock (AAPL)

## 1. Risk Factor Model Estimation
This tutorial serves as an introduction to quantitative finance and how to estimate the Fama French Carhart four-factor risk model exposures for an arbitrary stock using live data in Python to build upon what I learned in the International Asset Management course I took while abroad. This project covers the process and common pitfalls of pulling live data from the Fama-French risk factor database and from Yahoo Finance and running a factor sensitivity estimation using linear regression.

### Theory
The Carhart 4-factor model builds upon the Fama-French factor model, which is a 3-factor model including the size of firms (Small Minus Big - SMB), the value premium (High Minus Low - HML), and excess return on the market (the portfolio's return less the risk-free rate of return). The additional factor in the Carhart model is momentum (MOM). 

The idea of evaluating a stock based on these four factors is to better understand differences in its expected returns and the amount of risk carried by a portfolio. Ultimately, one can build a strategy around the findings to build a portfolio, which is the basis of factor investing.

### Methodology
It is first imperative to import the necessary to import the Pandas library to manipulate data retrieved by the Yahoo Finance Application Programming Interface (API). For visualization purposes, Matplotlib was used.

Next, the different Fama-French risk factor portfolio data libraries to select the ones most interested in, namely the Fama-French 3-factor model as well as the Carhart model which adds the fourth factor we are interested in (momentum) were retrieved using Pandas.

After importing general market data, the dates most desired to be analyzed were chosen, namely the earliest date possible to the present day.

Before adding in MOM as a fourth factor, the 3 risk factors were plotted to examine any trends that may have occurred. Due to the granularity of the data, a moving average was applied to smooth the time series data to better observe said trends.

Next, the Yahoo Finance package was installed to collect data on a particular stock, notably Apple Inc. (AAPL), with market data as earliest as its IPO date. It was then required to clean the data with Pandas in order to merge the AAPL stock data with the Fama-French-Carhart model general market data.

Finally, an OLS regression model was applied to the AAPL data to evaluate which factors caused the most variation (i.e. risk) in the portfolio.

### Findings
The most significant factors affecting AAPL were shown to be the market risk-free rate as well as the value factor (HML).

### Sources
YouTube Tutorial: https://www.youtube.com/watch?v=gN7JOFOO-eM&ab_channel=TechFin
