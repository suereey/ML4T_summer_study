# 01-07: Sharpe ratio and other portfolio statistics
## Daily protfolio value
- start_value = 1000000
- start_date = 2009-01-01
- end_date = 2011-12-13
- symbols = ['SPY', 'XOM', 'GOOG', 'GLD']
- ALLOCS = [0.4, 0.4, 0.1, 0.1] 
## How to calculate the total value of the portfolio day by day
![DailyPortfolio](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/07_DailyPortfolioValue.PNG)
## Portfolio statistics
- Daily return
- cumulative return
- average daily return
- std daily return
- sharp ratio: a metric that adjust return for risk
- All else being equal:
    - Lower risk is better
    - Higher return is better
- Sharp ratio considers: risk free rate of return (0% in bank)

![portfoliostatistics](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/07_PorfolioStatistics.PNG)

## Sharp ratio
### Form of sharp ratio
- Consider we have 3 factors, what is the best formula?
    - Portfolio return (Rp)
    - Risk free return (Rf)
    - Std of portfolio return (σp)
- Answer: (Rp-Rf)/σp

