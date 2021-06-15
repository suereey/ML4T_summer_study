# Dealing with Data
## How data is aggregated
- Many trades are happening on different exchanges, how shall we combine, analyze, and use them?
- Tick: The finest resolution of data is called a tick. A tick represents a successful buy sell match or a successful transaction.
- Example, figure below, in each time period, we have:
    - Open: 1 st one 
    - High: highest one
    - Low: lowest one
    - close: last one
    - volumn: total volumn during that time period.
    ![aggregatedata](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/47_aggregatedata.PNG)

## Price anomaly
- Stock split example:
    ![stocksplit](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/48_priceanomaly.PNG)
- Stock splits result in reduced price per unit.
For instance, say each stock unit is divided into two units, then the value of each new unit drops to half. This is what likely happened.
- Why stock split? **Price too high**
- Solution: **Adjusted close**
    - Explain
    ![stocksplit_explain](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/49_priceanomaly.PNG)
    - Example of the split adjustment
    ![splitadjustment](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/50_priceanomaly.PNG)

## Dividens
- Dividens
![dividen_1](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/51_dividen.PNG)
- Adjusting for dividens. The adjusted closing always equals to actual closing. Then based on the closing to adjust the previous value. In this case, different closing time you are looking at (2015 or 2012) may cause a different adjusted value (at 2010).
![adjustdividen](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/52_dividen.PNG)

## Survivor bias
![survivorbias](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/53_survivorbias.PNG)