# Put–Call Parity on Pepsi (PEP)
This project demonstrates how put–call parity links theoretical Black–Scholes prices to market option quotes. Using Pepsi (PEP) as the underlying stock, the analysis combined historical price context, theoretical verification under the Black–Scholes model with dividends, and real market option chain data retrieved from Yahoo Finance.

# Summary
Data Source: Yahoo Finance (PEP stock prices and option chains)
As-of Date: March 14, 2025
Expiry Analyzed: April 17, 2025
Theoretical Analysis: Verified that $C - P = S e^{-qT} - K e^{-rT}$ holds under Black–Scholes pricing across a strike grid
Market Analysis: Computed $C_{\text{mid}} - P_{\text{mid}}$ from option chain mid quotes and compared against the theoretical RHS with a bid–ask band
Findings: Most observed deviations were within the bid–ask band, consistent with transaction costs; out-of-band cases were tied to illiquid strikes or after-hours quotes

# Tools & Packages
Python & Jupyter/Colab
yfinance
pandas
numpy
matplotlib
scipy.stats

# Project Structure
pep_put_call_parity.ipynb: Main notebook with full analysis (stock context, theoretical parity, market parity)
artifacts/: Folder containing saved CSV tables and plots for both theoretical and market parity
README.md: Project overview

# Results
The theoretical analysis confirmed put–call parity under Black–Scholes with dividends. Market data showed that real-world deviations generally remained within bid–ask bounds, supporting efficient market behavior once transaction costs were considered.

# How to Run
To reproduce this project:

# Clone this repository or download the ZIP
Open pep_put_call_parity.ipynb in Jupyter or Google Colab
Ensure Python packages in requirements.txt are installed
Run all cells to generate plots and CSV outputs
Artifacts will be saved to the artifacts/ folder
View Project Deliverables
Notebook (HTML or Colab link): Full analysis including code, plots, and commentary
CSV Tables: Theoretical and market parity results
Plots: Price/return context, theoretical parity differences, market deviations vs bid–ask bands

#Author
Sathvika Parimi  
B.S. Financial Mathematics and Statistics, UC Santa Barbara
