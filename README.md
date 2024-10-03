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
