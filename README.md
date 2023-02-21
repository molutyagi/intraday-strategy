# bullsalgo

{if `jupyter notebook` command does not work, try `python3 -m notebook` it works absolutely fine}

An Intraday Trading Strategy Algorithm

The ScriptData class is used to retrieve and store the intraday data for a given stock symbol. The fetch_intraday_data method uses the alpha_vantage library to retrieve the intraday data for the given symbol, and the convert_intraday_data method converts the raw data into a pandas dataframe and formats it for easier use. The class also implements the __getitem__, __setitem__, and __contains__ methods for convenient access to the stored intraday data.

The indicator1 function calculates the moving average of the closing price for a given time period and returns the result as a dataframe with two columns: 'timestamp' and 'indicator'.

The Strategy class is used to implement the trading strategy. The fetch_data method retrieves the intraday data using the ScriptData class and calculates the moving average using the indicator1 function. The generate_signals method uses the moving average and the closing price to generate 'BUY', 'SELL', or 'NO_SIGNAL' signals based on a MA crossover strategy. The run method calls the generate_signals method to generate the signals and then prints the resulting signals dataframe.

I tried using pyalgotrading to plot the chart but I was getting "no module errors".

To run the code all you need to do is setup your venv and install all the requirements. Now simply call the strategy class with a script as an input and then call run method on it.
