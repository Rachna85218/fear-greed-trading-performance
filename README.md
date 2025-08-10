# fear-greed-trading-performance
Nice — below is a polished **README.md** you can drop straight into your GitHub repo.
I included your requested author and email exactly as you gave them.

You can copy-paste the Markdown below into a `README.md` file in your project.

---

# Market Sentiment vs Trade Performance Analysis

**One-line:** Analysis of how the Fear & Greed Index (market sentiment) relates to trade profitability, win-rates, and trade activity — with actionable insights and recommendations.

---

## Contents

* `notebook.ipynb` ,'dataset' — Clean, documented Jupyter/Colab notebook with full code, plots, and narrative.
* `fear_greed_index.csv` — Fear & Greed Index data (Date, Value, Classification).
* `historical_data.csv` — Historical trade data (Account, Coin, Execution Price, Size, Side, closed\_pnl, timestamps, etc.).
* `market_sentiment_analysis_with_visuals.docx` — Word report containing methodology, results, visuals commentary, insights & recommendations.
* `README.md` — This file.

> **Note:** Filenames above match those used in the analysis. If your filenames differ, update the notebook and README accordingly.

---

## Author

**Rachna**
Email: `rv124936&@gmail.com`

---

## Project Overview

This project merges daily Fear & Greed Index classifications with trade-level historical data to evaluate whether market sentiment affects:

* Average closed PnL,
* Win rate (percent profitable trades),
* Trade volumes and size patterns,
* Profitability by trade side and start position.

Key outputs include summary tables, statistical tests, and visualizations: boxplots (PnL distribution), bar charts (win rate, volume), scatterplots (trade size vs PnL), time series of trade sizes, and correlation heatmaps.

---

## Highlights / Key Insights

* **Fear** phases show the **highest average PnL** (≈ \$235.33) and strong profitability despite lower trade volumes.
* **Neutral** phases exhibit the **highest win rate** (≈ 45.86%) — consistent smaller gains.
* **Greed** phases have the **largest trade volumes** but **lower average PnL**, suggesting lower return-per-trade during bullish enthusiasm.
* **Extreme Fear / Extreme Greed** are more volatile with higher variance in outcomes.
* No statistically significant difference in average PnL between Fear and Greed (t-test p ≈ 0.2338).
* Trade size is not strongly correlated with profit — large trades do not reliably deliver larger profits.

---

## High-Impact Recommendations

1. **Scale moderately in Fear phases** — increase exposure but retain strict risk controls (stop-loss, position sizing).
2. **Deploy systematic strategies in Neutral phases** to harvest consistent small wins.
3. **Be selective in Greed phases** — avoid overtrading; focus on high-probability setups.
4. **Tighter risk controls for extremes** — narrower stop-loss/take-profit and smaller position sizing for Extreme Fear/Greed.
5. **Investigate Greed inefficiency** — deeper analysis into trade-level behavior during high-volume Greed days.

---

## How to run (Colab / Local)

### Colab (recommended)

1. Open [Google Colab](https://colab.research.google.com/) and upload `notebook.ipynb` or open it from your Drive.
2. Upload both datasets when prompted: `fear_greed_index.csv` and `historical_data.csv`.
3. Run cells sequentially. Plots will render inline.

### Local (Jupyter)

1. Create a Python environment (recommended: conda or venv).
2. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scipy python-docx
   ```
3. Place `notebook.ipynb`, `fear_greed_index.csv`, and `historical_data.csv` in the same folder.
4. Launch Jupyter:

   ```bash
   jupyter notebook
   ```
5. Open `notebook.ipynb` and run cells.

---

## Reproducibility & Notes

* The notebook contains clearly labeled Markdown sections explaining each step (what & why), and well-commented code blocks.
* The merging logic maps trade `trade_date` to the daily sentiment `date` — missing sentiment days are forward-filled to avoid dropping trade rows.
* Numeric conversion and deduplication steps are included for safe reproducibility.
* If your historical timestamps are in multiple formats (IST text and UNIX), the notebook tries both and selects the best parsed timestamp.

---

## Further Work / Next Steps

* Analyze performance per coin/token and per-account to see whether sentiment effects are asset-specific.
* Build risk-adjusted metrics (Sharpe, Sortino, max drawdown) per sentiment bucket.
* Create a strategy-simulator that backtests simple rules (e.g., increase position by X% during Fear) to estimate forward returns and drawdowns.
* Add automated alerts (Slack/Email) for significant sentiment regime changes combined with trade-size spikes.

---

## Contact

If you have questions or want this packaged for a presentation, contact:

**Rachna** — `rv124936&@gmail.com`

