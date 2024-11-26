# Managed Futures Fund Simulation with Rollover Strategy

This project simulates the performance of a **Managed Futures Fund (MF)** with the following parameters:

- **Strategy**: Long-only position on the second nearby WTI futures contract.
- **Nominal Capital**: The fund starts with **$10M** on **January 1, 2000**.
- **Collateralized Position**: Assumes fully collateralized positions with 100 contracts (each contract represents 1,000 barrels of oil). If the oil price is $100, the fund can hold 100 contracts.
- **Rollover Mechanism**: The fund rolls over the futures contract 5 business days before the expiration date to the third nearby contract, and then 5 business days later, the third contract becomes the second contract.
- **Market Data**: The simulation uses market data for WTI futures and SPX for performance analysis.

## Key Features:

- **Long-only Position**: The strategy remains long on the second nearby WTI contract throughout the simulation, benefiting from price increases.
- **Rolling Over Contracts**: The strategy automatically rolls over contracts 5 business days before expiration to the third nearby, and after 5 business days, the third contract becomes the second nearby.
- **Risk Management**: The portfolio is fully collateralized, and contracts are adjusted to maintain exposure to the underlying asset while managing expiration risk.
- **Performance Analysis**: The project includes a **1-year rolling regression analysis** of the MF fund’s returns against the SPX (S&P 500) index, based on weekly returns. This helps assess the fund's correlation and risk exposure to the broader market.

## Assumptions:

1. The strategy is implemented as a **long-only** position in WTI futures.
2. The fund is fully collateralized and assumes no margin calls or liquidations.
3. The **rollover mechanism** ensures continuous exposure to the WTI market by switching to the third nearby contract ahead of expiration.
4. The **risk-free rate** is used as the monthly risk-free rate for interest accruals.
5. The **oil price** and **lot size** are used to calculate the number of contracts held in the portfolio.


### Data Sources:
- **WTI Futures Data**: Downloaded using the `yfinance` library.
- **SPX and VIX Data**: Also sourced from `yfinance` for analysis and implied volatility.

## Results and Outputs:
- The simulation provides both **monthly PnL** and **cumulative PnL** for the portfolio, showing the impact of the long position and contract rollover strategy.
- The **1-year rolling regression** of the Managed Futures Fund’s returns against SPX gives insights into the correlation and risk-adjusted returns of the strategy.
