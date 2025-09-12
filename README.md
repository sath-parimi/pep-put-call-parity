# Empirical Analysis of Put–Call Parity on PepsiCo Options

This project demonstrates and tests the put–call parity relationship using PepsiCo (PEP) options as a case study. Put–call parity is a core principle of options pricing, linking theoretical Black–Scholes values to real market quotes. The notebook provides both a worked example (PepsiCo, Sept 2025) and a generalizable framework that users can adapt to any listed stock.

## Summary
- **Data Source:** Yahoo Finance (PEP stock prices and option chains)  
- **As-of Date:** September 11, 2025  
- **Expiry Analyzed:** September 12, 2025  
- **Theoretical Analysis:** Verified that $C - P = S e^{-qT} - K e^{-rT}$ holds under Black–Scholes with dividends, to numerical precision (~1e-14). 
- **Market Analysis:** Compared mid–quote values of calls and puts against theoretical parity, with deviations bounded by bid–ask spreads.
- **Findings:** 
  - Theoretical parity holds exactly (machine precision).  
  - Market data showed differences, but they remained inside the bid–ask tolerance band.  
  - Observed “violations” are due to transaction costs, spreads, and liquidity, not arbitrage.  

## Tools & Packages
- Python (Google Colab)
- `yfinance`
- `pandas`
- `numpy`
- `matplotlib`
- `scipy.stats`

## Project Structure
- `pep_put_call_parity.html`: Full report of PepsiCo case study (Sept 11-12, 2025)
- `put_call_parity.ipynb`: Generic notebook (reusable framework for any stock) 
- `README.md`: Project overview

## Results
The theoretical analysis confirmed put–call parity under Black–Scholes with dividends. Market data showed that real-world deviations generally remained within bid–ask bounds, supporting efficient market behavior once transaction costs were considered.

## How to Run
To reproduce this project:
1. Clone this repository or download the ZIP.
2. Open `put_call_parity.ipynb` in Jupyter or Google Colab.
3. Ensure Python packages listed are installed.
4. Change the `TICKER` parameter to any Yahoo Finance ticker (default is `"PEP"`, but try `"AAPL"`, `"MSFT"`, `"TSLA"`, etc.).
5. Update financial parameters `r` (risk–free rate) and `q` (dividend yield) as needed.
6. Run all cells to generate plots and tables.

## View Project Deliverables
- [Full PepsiCo Analysis Report (HTML)](https://sath-parimi.github.io/pep-put-call-parity/pep_put_call_parity.html): Full report including code, plots, and commentary
- [Generic Notebook (IPYNB)](https://sath-parimi.github.io/pep-put-call-parity/put_call_parity.ipynb): Reusable framework with guidance for any stock 

# Author
Sathvika Parimi  
B.S. Financial Mathematics and Statistics, UC Santa Barbara
