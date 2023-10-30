# Portfolio Optimization Tool

This project utilizes historical stock data to calculate the efficient frontier of portfolios, allowing users to visualize and understand the risk and return trade-offs. The code fetches stock data from Yahoo Finance, calculates expected returns and covariance matrix, and then uses different methods and visualizations to optimize and display the portfolios.

## Features

1. **Fetch Stock Data**: Uses `yfinance` to fetch historical stock data for specified tickers from Yahoo Finance.
2. **Calculate Expected Returns & Covariance Matrix**: Using historical data to compute the annualized mean historical return and the sample covariance matrix.
3. **Efficient Frontier**: Utilizes the `EfficientFrontier` object from `pypfopt` to compute portfolios that maximize the Sharpe ratio.
4. **CLA (Critical Line Algorithm)**: Another method to optimize portfolios, especially useful when the number of assets is large.
5. **Visualization**: Displays the efficient frontier, highlighting the portfolio with the maximum Sharpe ratio.
6. **Portfolio Weights Adjustments**:
    - Default (0 to 1) representing long-only portfolios.
    - (-1 to 1) allowing short positions.
    - Custom bounds for capping maximum or minimum weights.

## Dependencies

- `pandas`
- `numpy`
- `yfinance`
- `pypfopt`
- `matplotlib`

## How to Use

1. Update the `tickers` variable with the stock tickers of your choice.
2. Run the code.
3. The various plots generated will showcase the efficient frontier, the portfolios with the maximum Sharpe ratio, and different portfolio weight scenarios.

## Notes

- The code has provisions to test portfolio optimizations using random weights and different bounds.
- For realistic results, ensure you're fetching data for the correct stocks and adjusting bounds as necessary.

## Future Work

- [ ] Integrate with other data sources apart from Yahoo Finance.
- [ ] Implement additional optimization techniques.

