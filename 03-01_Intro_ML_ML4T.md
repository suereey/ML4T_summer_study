# How Machine Learning is used at a hedge fund
## General intro: the machine learning
![MLproblem](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/01_GeneralMLproblem.PNG)
## Supervised regression learning
- Supervised: provice example X, Y
- regression: numerical prediction
- learning: train with data
- Different methods:
    - Linear regression (parametric: *Slow training but fast inquiry*)
        ![parametric](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/07_Regression_Parametric.PNG)
    - Knearest neighbor (KNN: *Fast training but slow inquiry*) (instance based)
        ![KNN](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/08_Regression_KNN.PNG)
    - Decision trees
    - Decision forests

Note: Difference between parametric and instance based method?

- In parametric, we take the data and merge around to come up with a few parameters, and then THROW data away.
- In KNN, we keep all the historical data, the X and Y pairs, when it's time to make a prediction, we consult that data.

## Stock data for ML
- Historical data:
![StockData](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/02_StockData.PNG)
- Example of a fintech company:
![Example_01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/02_StockData.PNG)
- Software example:
![Software](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/04_SoftwareExample.PNG)

## Backtesting to check the accuracy
![Backtest](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/05_Backtesting.PNG)

## Problems with regression in real world
- Result always noisy and uncertain
- Challenging to estimate the confidence
- Hard to know the holding time and allocation

So later in this class will learn: Policy learning RL.

## Summary: Future class we will focus on 

![Future](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/06_FutureClassFocus.PNG)

