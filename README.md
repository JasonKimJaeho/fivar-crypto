# fivar-crypto
Application of the FIVAR paper's methodology to the crypto market using Binance coin data. Includes a performance comparison between H-LASSO, EWMA, HAR-DRD, and HAR-DRD-LOG models.


### Project Workflow & File Structure

**1. `make_univrse.ipynb**`

* **Description:** Selects the top 200 cryptocurrency tickers based on liquidity to form the initial universe.
* **Output:** `crypto_universe_output/final_tickers_formation_2023_2025_top200.csv`

**2. `filter_universe.ipynb**`

* **Description:** Processes the log price data and removes dates with excessive missing values (e.g., drops data from 2023-03-24).
* **Output:** `crypto_universe_output/log_price_2023_2025_top200.parquet`

**3. `PRVM.ipynb**`

* **Description:** Calculates the PRVM (Proxy for Realized Volatility Matrix) for the selected universe.
* **Output:** `crypto_prvm_output/prvm_gamma_jv_2023_2025_top200.npz`

**4. `FIVAR_HAR**`

* **Description:** The main execution file that models the data (comparing H-LASSO, EWMA, HAR-DRD, and HAR-DRD-LOG).

---

**Tip:** If `make_univrse.ipynb` is a typo in your actual file name (missing an 'e'), you might want to rename the file to `make_universe.ipynb` in your repository before committing, and update the README accordingly!
