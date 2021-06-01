# Being Hedge Fund Manager
## More about funds
- Types of funds: 3 major types
    - ETF: exchange traded funds
    - Mutual Fund
    - Hedge Fund


- Key words:
    - Liquid: how easy one can buy/sell shares in a particular holding. 
        - Stocks are extremely liquid, ETF  as well
        - ETF is liquid in many ways:
            - easy trading
            - ETFs with higher volumes are more liquid
    - Large "cap":
        - cap = capitalization: how much a company worth according to shares that are outstandin times the price of the stock. (#shares*prices)

![fundtype](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/1_generalintro.PNG)

- What type of fund it is?
    - Mutual Fund: 5 letters
    - ETF: 3 or 4 letters
    - Hedge Fund: no abbreviations.
![fundname](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/2_Fundsname.PNG)

- Incentives: How are they compensated?
    - AUM: Assets under management: how much money is being managed by the funds
    - Different compensate:
        - Expense ratio: a ratio of AUM
        - Two and twenties
    ![compensate](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/3_compensate.PNG)
    - Note: two and twenty. 
        - 2% aum + 20% profit
        - example calculation
        ![calculation](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/4_twotwenty.PNG)
    - Different compensate gives different incentives
    ![incentives](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/5_incentives.PNG)

- How funds attract investors, who and why
    - Who?
        - Individuals
        - Institutions
        - Funds of funds
    - Why?
        - Track record (5 yrs of good record)
        - Simulation + story
        - Good portfolio fit

- How fund goals and metrics:
    - Goals:
        - Beat a benchmark, for example SP500.
        - Absolute return, provide positive return, no matter what. (Long/short)
    - Metrics: How to measure how well the funds match the goal
        - Cumulative return = (val[-1]/val[0])-1
        - Volatility = daily_rets.std()
        - Risk/Reward = *sharpe ratio*
- Computing inside a hedge fund
    ![computing_01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/07_computing.PNG)
    ![computing_02](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/08_computing.PNG)
    ![computing_03](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/09_computing.PNG)
