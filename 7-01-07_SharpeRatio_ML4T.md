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
- sharpe ratio: a metric that adjust return for risk
- All else being equal:
    - Lower risk is better
    - Higher return is better
- Sharpe ratio considers: risk free rate of return (0% in bank)

![portfoliostatistics](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/07_PorfolioStatistics.PNG)

## Sharpe ratio
### Form of sharpe ratio
- Consider we have 3 factors, what is the best formula?
    - Portfolio return (Rp)
    - Risk free return (Rf)
    - Std of portfolio return (σp)
- Answer: (Rp-Rf)/σp
### Computing sharpe ratio
- Step 1: 

    S = E[Rp-Rf]/std[Rp-Rf], where E is expected

    S = mean(daily_return - daily_riskfree)/std(daily_return - daily_riskfree)

    what is thet risk free rate: LIBOR, 3 month T-Bill, 0% (used in this class)

    daily_riskfree = 0

    **S = mean(daily_return - daily_riskfree)/std(daily_return)**

- Step 2: Sharpe ratio vary widely depending on how frequently you sample
    - Sharpe ratio (SR) is an annual measure
    - SR annualized = k * SR
    - K = (# samples per year)^0.5
        - Daily K = (252)^0.5
        - Weekly K = (52)^0.5
        - Monthly k = (12)^0.5
    - **S = 252^0.5*mean(daily_return - daily_riskfree)/std(daily_Sreturn)**
- Calculation example:
![sharperatiocalculation](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/07_CalculationExample_SharpeRatio.PNG)
## Summary
- Important Statistics
    - Cumulative return
    - Average daily return
    - Std (Risk)
    - Sharpe ratio