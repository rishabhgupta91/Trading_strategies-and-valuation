# Simulation of Moving Average Crossover Trading Strategy with Python

The strategy aims to identify potential buy and sell signals based on the crossover of two moving averages, a short-term 30-day moving average (30d MA) and a longer-term 90-day moving average (90d MA).

## Trading Logic:

Initialize variables to track the trading position (long or flat), available cash, owned shares, buy signals, and sell signals.
Iterate through the historical data, row by row, to apply the trading strategy.
If the 30-day moving average is below the 90-day moving average and there is no existing position (position == 0), a buy signal is generated.
Calculate the number of shares that can be purchased with available cash and update the trading position.
If the 30-day moving average is above the 90-day moving average and there is an existing long position (position == 1), a sell signal is generated.
Calculate the cash obtained from selling the owned shares, reset the trading position to flat, and clear the shares owned.
The buy and sell signals are counted to monitor the trading activity.

## Key Takeaways:

The moving average crossover strategy aims to capture trends by identifying points where shorter-term trends cross above or below longer-term trends.
Buy signals suggest potential opportunities to enter a long position, while sell signals indicate potential exits from a long position.
The strategy's effectiveness can vary based on the chosen timeframes for moving averages and the specific stock being analyzed.
