# Managed Futures Fund Simulation with Rollover Strategy

This project simulates the performance of a **Managed Futures Fund (MF)** with the following parameters:

- **Nominal Capital**: The fund starts with **$10M** on **January 1, 2000**.

- **Transaction Costs**: A 0.05% fee applies to all rollovers.
- **Margin Requirement**: A 10% margin requirement is enforced to ensure adequate collateral against positions.
- **Collateral Interest**: Unused collateral earns a 4% annualized risk-free interest rate.

## Key Features:

- **Strategy**: Long-only position on the second nearby WTI futures contract.
- **Rollover Mechanism**: Contracts are rolled over 5 business days before expiration to the third nearby. After 5 days, the third nearby becomes the second nearby.
- **Performance Analysis**: The project includes a **1-year rolling regression analysis** of the MF fund’s returns against the SPX (S&P 500) index, based on weekly returns. This helps assess the fund's correlation and risk exposure to the broader market.

## Assumptions:

1. Futures data is continuous, with no data gaps or irregularities.
2. The **risk-free rate** is a constant 4%

### Data Sources:
- **WTI Futures Data**: Downloaded using the `yfinance` library.
- **SPX Data**: Also sourced from `yfinance` for analysis and implied volatility.
