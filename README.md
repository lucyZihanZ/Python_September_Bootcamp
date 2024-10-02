# Python_September_Bootcamp
### Description:

1. **StockMarket Class**:
   - It has a method named `advance_one_day` which simulates the stock market for one day. If the price of a stock drops below $0.01, you will no longer be able to trade it, and the number of shares of that stock in your portfolio will become 0.
   - It has a method named `get_stock_prices` which returns the current stock price.

2. **Portfolio Class**:
   - This class is provisws as-is. DO NOT modify this class.
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
       - Update stocks attribute.

3. **Strategy**:
   - For each day until day 100:
     - Use `get_stock_prices` method to get the current stock prices.
     - Decide whether to buy/sell stocks based on the current stock prices.
     - Use `advance_one_day` method to move to the next day.
   - You may write any helper functions you need, as long as you don't change the code of both classes.
   - Your goal is to have as much money as possible by the end of day 100.

**Steps**:

1. Initialize the stock market and your portfolio.
2. Loop through each day and make buy/sell decisions.
3. Use the `advance_one_day` function to progress through the simulation.
4. At the end of day 100, compute and print the total value (cash and stock values) of your portfolio.
