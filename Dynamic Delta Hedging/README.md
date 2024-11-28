# Dynamic Delta Hedging

## Overview

This project analyzes the performance of dynamic delta hedging strategies applied to S&P 500 Index (SPX) options. By leveraging volatility indices, this study explores the effectiveness of delta hedging under varying market conditions.

---

## Project Structure

- **Code Files:** Python notebook implementing hedging strategy, data preprocessing, and analysis.
- **Data:** VIX volatility indices, SPX option expiration dates  and associated risk-free rates.
- **Results:** Outputs include hedging error statistics categorized by deltas and financial crisis periods.

---

## How to Use

1. **Setup Environment**
   - Install required Python libraries: `numpy`, `pandas`, `matplotlib`, and `scipy`.
   - Ensure the notebook has access to the input datasets (price data and volatility indices).

2. **Run Analysis**
   - Open the Jupyter notebook file `SPX_Delta_Hedging.ipynb`.
   - Execute cells sequentially to replicate the delta hedging simulations and statistical analysis.

3. **Interpret Results**
   - Review generated plots and tables that summarize the hedging error across different configurations.
---

## Future Work

This project can be extended by:
- Including additional asset classes or derivatives.
- Experimenting with alternative volatility models or options pricing methods.
- Analyzing dynamic hedging under extreme market events.

---

## License

This project is licensed under the [MIT License](LICENSE).

