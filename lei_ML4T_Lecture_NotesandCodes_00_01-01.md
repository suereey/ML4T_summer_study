# 00-00 Introduction
## Three parts to the course
1. Manipulating financial data in python
2. Computational investing
3. Learning Agorithms for trading

## Three textbooks
1. Python for Finance by Hilphish
2. What Hedge Funds Really Do
3. Machine Learning by Mitchell

# Reading and plottign stock data 01-01
## CSV file of stock data
which fields would you expect to see in a csv file of stock data? 

Answer: data/time, price of the stock


## Real stock data and Pandas data frame
### Stock data example 
![csv example](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/01_csv_data.PNG?token=AJQS7UTPVFRR4G3VGNYWKIDAUP72A)

### Pandas data frame example
![Pandas example](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/01_pandas_datafram.PNG?token=AJQS7UVE7TEAFXHBIYL3PJ3AUP76I)

## Code implementation
### Read csv file and select roles

```
import pandas as pd

def test_run():
    """Function called by Test Run."""
    df = pd.read_csv("data/AAPL.csv")
    print df		    # prints entire data set (dataframe)

    print df.head()		# prints first five records
    print df.tail()	    # prints last five records
    print (df[10:21])	# print rows between index 10 and 20 inclusive

if __name__ == "__main__":
    test_run()
```

### Compute max closing price
```
import pandas as pd

def get_max_close (symbol):
    """Return the maximum closing value for stock indicated by symbol.

    Note: Data for a stock is stored in file: data/<symbol>.csv
    """
    df = pd.read_csv("data/{}.csv".format(symbol))  # read in data
    return  df['Close'].max() # compute and return max
  
def test_run():
    """Function called by Test Run."""
    for symbol in ['AAPL', 'IBM']:
        print ("Max close")
        print (symbol, get_max_close(symbol))


if __name__ == "__main__": # if run standalone
    test_run()
	
```

### Compute mean volume
```
import pandas as pd
import matplotlib.pyplot as plt
	
def get_mean_volume(symbol):
    """Return the mean volume for stock indicated by symbol.
    Note: Data for a stock is stored in file: data/<symbol>.csv
    """
    df = pd.read_csv("data/{}.csv".format(symbol))  # read in data
    # Quiz: Compute and return the mean volume for this stock
    return df['Volume'].mean()
   
def test_run():
    """Function called by Test Run."""
    for symbol in ['AAPL', 'IBM']:
        print ("Mean Volume")
        print (symbol, get_mean_volume(symbol))

		
if __name__ == "__main__":
    test_run()
```

### Plot stock price data
```
import pandas as pd
import matplotlib.pyplot as plt

def test_run():
    """Plot a single column."""
    df = pd.read_csv("data/AAPL.csv")
    print (df['Adj Close'])
    df['Adj Close'].plot()
    plt.show()  # must be called to show plots


if __name__ == "__main__":
    test_run()
```
### Plot high prices for IBM
Similar to the above plot stock price data
```
def test_run():
    df = pd.read_csv("data/IBM.csv")
    # Quiz: Your code here
    print (df['High'])
    df['High'].plot()
    plt.show()  # must be called to show plots

```

### Plot two columns
Similar to the above plots
```
def test_run():
    df = pd.read_csv("data/IBM.csv")
    df[['Close', 'Adj Close']].plot()
    plt.show()  # must be called to show plots
```