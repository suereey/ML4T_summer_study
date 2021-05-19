# 01-04 Statistical analysis of time series
## Compute global statistics
Lei insert figure
- compute mean: df.mean()
- compute median: df.median()
- compute std: df.std()

get data:
```
import os
import pandas as pd
import matplotlib.pyplot as plt

def symbol_to_path(symbol, base_dir="data"):
    """Return CSV file path given ticker symbol."""
    return os.path.join(base_dir, "{}.csv".format(str(symbol)))

def get_data(symbols, dates):
    """Read stock data (adjusted close) for given symbols from CSV files."""
    df = pd.DataFrame(index=dates)
    if 'SPY' not in symbols:  # add SPY for reference, if absent
        symbols.insert(0, 'SPY')

    for symbol in symbols:
        df_temp = pd.read_csv(symbol_to_path(symbol), index_col='Date',
                parse_dates=True, usecols=['Date', 'Adj Close'], na_values=['nan'])
        df_temp = df_temp.rename(columns={'Adj Close': symbol})
        df = df.join(df_temp)
        if symbol == 'SPY':  # drop dates SPY did not trade
            df = df.dropna(subset=["SPY"])
    return df
```
plot:
```
def plot_data(df, title="Stock prices"):
    """Plot stock prices with a custom title and meaningful axis labels."""
    ax = df.plot(title=title, fontsize=12)
    ax.set_xlabel("Date")
    ax.set_ylabel("Price")
    plt.show()
```
calculation
```
def test_run():
	# Read data
	dates = pd.date_range('2010-01-01', '2012-12-31')
	symbols = ['SPY', 'XOM', 'GOOG', 'GLD']
	df = get_data(symbols, dates)
	plot_data(df)
	
	# Compute global statistics for each stock
	print (df.mean())
	print (df.median())
	print (df.std())

if __name__ == "__main__":
    test_run()
```
## Rolling statistics
- rolling mean vs global mean
Lei insert figure 2 figrues
- compute rolling statistics
```
	# Plot SPY, retain matplotlib axis object
	ax = df['SPY'].plot(title="SPY rolling mean", label='SPY')
	
	# Compute rolling mean using a 20-day window
	rm_SPY = df['SPY'].rolling( window=20).mean()
	
	# Add rolling mean to same plot
	rm_SPY.plot(label='Rolling mean', ax=ax)
	
	# Add axis labels and legend
	ax.set_xlabel("Date")
	ax.set_ylabel("Price")
	ax.legend(loc='upper left')
	plt.show()
```
## Bollinger Bands

'''
def get_rolling_mean(values, windows):
    """Return rolling mean of given values, using specified window size."""
    return values.rolling( window=windows).mean()

def get_rolling_std(values, windows):
    """Return rolling standard deviation of given values, using specified window size."""
    # Quiz: Compute and return rolling standard deviation
    return values.rolling(window=windows).std()

def get_bollinger_bands(rm, rstd):
    """Return upper and lower Bollinger Bands."""
    # Quiz: Compute upper_band and lower_band
    upper_band = rm + rstd * 2
    lower_band = rm - rstd * 2
    return upper_band, lower_band
'''

