# Stock_price_simulation

1.**StockMarket Class**: 
   - It has a method named `advance_one_day` which simulates the stock market for one day. If the price of a stock drops below $0.01, you will no longer be able to trade it, and the number of shares of that stock in your portfolio will become 0.
   - It has a method named `get_stock_prices` which returns the current stock price.

2.**Portofolio Class**:
   - **Attributes**:
     - `cash`: the amount of money you currently have.
     - `stocks`: number of different stocks you currently own.
   - **Methods**:
     - `buy`: purchase k shares of a given stock.
       - Input: ticker of the stock (`stock_ticker`), number of shares (`k`), the current price of the given stock (`stock_price`).
       - Deduct cash by `(stock price * k) + 0.50` (50 cents fee for each transaction).
       - Update stocks attribute.
     - `sell`: sell k shares of a stock.
       - Input: ticker of the stock (`stock_ticker`), number of shares (`k`), the current price of the given stock (`stock_price`).
       - Add to cash by `(stock price * k) - 0.50` (50 cents fee for each transaction).

3.**Strategy**:

   At the beginning, an initial cash amount of $1000 is allocated to a portfolio (Portfolio), which interacts with the stock market (StockMarket) through predefined stock tickers (STOCK_TICKERS). The function get_the_rate() calculates the rate of increase or decrease in stock prices by comparing the prices of two consecutive days. The strategy is implemented through a loop that runs for 100 days. On each day, the algorithm compares the stock prices from the current and previous days. It calculates the rate of change for each stock ticker, then selects the stock with the maximum rate of increase (max_ticker) and the one with the maximum decrease (min_ticker). The decision to buy or sell depends on the absolute value of these rates.


# NBA_players'_information_analysis

The task involves performing data analysis on two CSV files, `"players.csv"` and `"salaries_1985to2018.csv"`, using `pandas`, `numpy`, `seaborn`, and `matplotlib`. The first step is to read both CSV files into separate dataframes and then merge them based on the player name, with a hint to rename one of the columns to facilitate the merge. Once merged, several analyses are performed on the combined dataframe.

First, a `line plot` of average salaries by season should be created to determine whether salaries have been increasing over time. Similarly, a line plot of the average `player weight` by season is needed to observe whether player weight has been increasing. Next, the average salary for each `draft pick round` is calculated to identify any trends. `Players' heights` should be divided into 2-inch buckets, starting from 6'0 (e.g., 6'0-6'2, 6'2-6'4), and a histogram of these height buckets should be plotted. The average `salary` for each height bucket will also be analyzed. Since heights are stored as strings, they may need to be converted to inches as integers for easier sorting, then back to strings when plotting.

Further analysis includes grouping by player ID to create a scatter plot of the average `career field goal percentage` (FG%) versus `effective field goal percentage` (eFG%). Converting the values from strings to floats may be necessary for accurate plotting. Finally, a similar grouping by player ID is used to make a scatter plot of average career `FG%` versus career free throw percentage (`FT%`), allowing for an investigation of any noticeable patterns or anomalies.


# Stock Price Analysis
Which stock should we buy?

1. **`companies.csv`**: A dataset containing details of S&P 500 companies.
    - **Columns**:
        - `Name`: Name of the company.
        - `Ticker`: Stock ticker symbol of the company.
        - `Sector`: Industry sector to which the company belongs.

2. **`stock_prices.csv`**: A dataset with daily stock prices for the past year for the companies listed in `companies.csv`.
    - **Columns**:
        - Company tickers derived from the `companies.csv` file.
    - **Note**: The values in this dataset may not be exclusively in float type. There could be instances of `strings` and `NaN` types, which need to be handled for certain tasks.


1. Plot Stock Prices vs. Time for Two Companies in One Plot:**

2. Plot Average Stock Price for Each Sector:**

First calculate the stock-level average price over the past year. Then, using the average of each stock over the past year, calculate the sector-level average price. Finaly, plot the sector-level average price. You can use any method of plotting.

Answer:*From the image, we can see that over the past year, the `Consumer Staples` sector had the highest average stock price at `316.80` dollars per stock, which means it has been the best for investment. The `Health Care` sector comes second, with an average stock price of `243.68` dollars per stock.*
