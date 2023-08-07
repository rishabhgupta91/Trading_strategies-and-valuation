# Simulation of Moving Average Crossover Trading Strategy with Python

The strategy aims to identify potential buy and sell signals based on the crossover of two moving averages, a short-term 30-day moving average (30d MA) and a longer-term 90-day moving average (90d MA).

## Trading Logic:

1. Initialize variables to track the trading position (long or flat), available cash, owned shares, buy signals, and sell signals.
2. Iterate through the historical data, row by row, to apply the trading strategy.
3. If the 30-day moving average is below the 90-day moving average and there is no existing position (position == 0), a buy signal is generated.
4. Calculate the number of shares that can be purchased with available cash and update the trading position.
5. If the 30-day moving average is above the 90-day moving average and there is an existing long position (position == 1), a sell signal is generated.
6. Calculate the cash obtained from selling the owned shares, reset the trading position to flat, and clear the shares owned.
7. The buy and sell signals are counted to monitor the trading activity.

## Key Takeaways:

1. The moving average crossover strategy aims to capture trends by identifying points where shorter-term trends cross above or below longer-term trends.
2. Buy signals suggest potential opportunities to enter a long position, while sell signals indicate potential exits from a long position.
The strategy's effectiveness can vary based on the chosen timeframes for moving averages and the specific stock being analyzed.



# Simulation of Pair Trading Strategy with Python

**Pair Trading Strategy for XOM and CVX**

**Aim of the Strategy:**
The aim of this pair trading strategy is to identify trading opportunities between two stocks, Exxon Mobil Corporation (XOM) and Chevron Corporation (CVX), by exploiting their historical price relationship. The strategy involves identifying instances when the spread between the stock prices diverges from its historical mean, then taking positions to capitalize on the expected mean reversion.

**Trading Logic:**
1. Calculate the normalized return index for each stock to create a common baseline.
2. Compute the squared deviations between the normalized price series of the two stocks to measure the price distance. (Choose the pairs with minimum Normalized Price Distance)
3. Perform a linear regression analysis to identify potential cointegration between the stock prices. (Analyzing the relationship between the stock prices to see if they move together in a similar way)
4. Use Z-scores of the spread between XOM and CVX prices to generate entry and exit signals. (a special score that tells us when the difference between XOM and CVX prices is big or small, and use this to decide when to start or stop trading)
5. When the Z score suggests that XOM is doing worse than usual and CVX is doing better, consider selling XOM and buying CVX. If the score says XOM is doing better and CVX is doing worse, consider selling CVX and buying XOM.
6. Close the positions when the Z-score crosses a specified exit threshold.

**Key Takeaways:**
1. Pair trading leverages the historical relationship between two correlated stocks.
2. The strategy seeks to profit from the mean reversion of the spread between stock prices.
3. Entry and exit signals are generated based on Z-scores to capture divergence and convergence patterns.
4. Backtesting and optimization can help refine entry and exit thresholds for better performance.
