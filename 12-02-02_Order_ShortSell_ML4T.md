# Market Mechanics
## Order
- What is in an order?
    - Buy or sell?
    - Symbol: identifier for your target ETF
    - number of shares: Stocks, ETFs and other assets are sold in units of shares, not by amount of money
    - Limit or Market
        - Market: willing to accept a good price but essentially whatever price the market is currently bearing
        - Limit: don't want to do any worse than a certain price
    - Price: market order cannot specify the price.
    - Example: 
        - (BUY, IBM, 100, LIMIT, 99.5) i want to buy 100 shares of IBM AT NO MORE THAN 99.95$
        - (sell, GOOG, 150, MARKET) i want to sell 150 google shares at market price
- Order book
![orderbook](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/10_orderbook.PNG)
![orderbook02](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/11_orderbook.PNG)
- How orders get to the exchange:
    - Supposely thourugh the exchanges (NYSE, NASDAQ, BATS)
    - Currently, >80/90% of transactions did not involve exchages. They were conducted through:  executed internally within a broker or filled using a Dark Pool
    ![orderexchange](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/12_OrderExchange.PNG)
- Order book exploit
    - Order book exploit:
    ![exploit_01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/13_orderbook_exploit.PNG)
    - Geographic arbitrage:
    ![exploit_02](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/14_orderbook_exploit.PNG)
- Additional order types
    - Exchanges
        - Buy Sell
        - Market Limit
    - Broker
        - Stop loss
        - Stop gain
        - Trailing stop
        - Sell short: take a negative position on a stock. You sell a stock short if you believe its price is going to go down. Keep in mind here, we are selling stock we don't even own. (Broker can do that)
- Mechanics of shortselling: Entry
    - If the price goes down, you gain money
    - If the price goes up, you loss money
    ![short01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/15_short.PNG)
    ![short02](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/16_short.PNG)

# What is company worth
## Company value
- The true value of company
    - Intrinsic value: based on if you own a share of stock, how many dividen you will get in the future.
    - Book value: based on assets that the company owns
    - Market cap: based on the value of stock on market, how many shares are outstanding
    ![value_01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/17_companyvalue.PNG)
- The value of a future dollar
    - intrinsic value:
        - P.V. (present value)
        - F.V. (future value)
        - IR (interest rate)
            - IR also relates to how risky the company is.
            - IR is related to __Discount Rate__
                - High Discount Rate: trust company less and more risky
        - i: how far in the future will this payment be delivered. 
            - pay now, i = 0, P.V. = F.V.
            - pay 1 year from now, i = 1.
        ![worth_01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/18_worthofadollar.PNG)
        ![worth_02](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/19_worthofadollar.PNG)
        ![worth_03](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/20_worthofadollar.PNG)

    - Book value: 
    ![bookvalue](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/21_bookvalue.PNG)
    - Market capitalization: __Market cap = #shares*price__

## Why informaiton affects stock price
![info](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/22_info.PNG)
## Would you buy the stock?
![wouldyoubuy_01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/21_woul%20you%20buy.PNG)
![wouldyoubuy_02](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/02_screenshot/23_woul%20you%20buy.PNG)

- normally book value > market cap. people will immedietly buy it if book value is smaller.
- market cap is affect by intrinsic value.
