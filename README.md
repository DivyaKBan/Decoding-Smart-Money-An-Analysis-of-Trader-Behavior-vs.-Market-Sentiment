# Decoding Smart Money: An Analysis of Trader Behavior vs. Market Sentiment

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Libraries](https://img.shields.io/badge/Libraries-Pandas%20%7C%20Seaborn%20%7C%20Scikit--learn-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 1. Project Overview

This project conducts a deep-dive analysis into the behavior and performance of over 30 unique traders across 200,000+ cryptocurrency trades. The core objective is to empirically test the famous trading maxim: **"Be fearful when others are greedy, and greedy when others are fearful."**

By merging granular trade data with the daily Fear & Greed Index, this analysis segments traders into performance tiers to identify the statistically significant behaviors that separate the elite "Smart Money" from the average market participant. The project progresses from data preparation and feature engineering to statistical validation, advanced visualization, and unsupervised machine learning to uncover data-driven, actionable insights.

---

## 2. Key Question & Hypothesis

**Primary Hypothesis:** Elite traders ("Top 5%") achieve superior returns by adopting contrarian strategies, actively buying during periods of market fear and reducing exposure during periods of market greed, while lower-performing traders follow the herd.

---

## 3. Data Sources

* **Trade Data (`historical_data.csv`):** An anonymized dataset of over 200,000 individual trades, containing details like account ID, trade size (USD), side (Buy/Sell), and Closed PnL.
* **Sentiment Data (`fear_greed_index.csv`):** A daily time-series of the Crypto Fear & Greed Index, providing a sentiment score from 0 (Extreme Fear) to 100 (Extreme Greed).

---

## 4. Methodology

The project follows a structured, multi-step analytical workflow:

1.  **Data Preparation:** The trade and sentiment datasets were cleaned, processed, and merged on the date to tag every trade with the market sentiment of that day.
2.  **Advanced Feature Engineering:** Traders were profiled to create performance metrics, including Total PnL, Win Rate, and a risk-adjusted return score (Sharpe Ratio proxy). Traders were then segmented into three tiers: **Top 5%**, **Average Trader**, and **Bottom 5%**.
3.  **Statistical Analysis & Modeling:**
    * Comparative analysis was performed to measure the performance of each tier across different sentiment categories.
    * An **ANOVA test** was conducted to statistically validate that the observed performance differences were not due to random chance.
    * **K-Means Clustering** was used to identify natural behavioral archetypes among traders based on their trading styles and performance metrics.
4.  **Visualization & Reporting:** Key findings were visualized using Seaborn and Matplotlib to tell a clear, data-driven story.

---

## 5. Key Findings & Visualizations

### Finding 1: Performance Polarizes in Extreme Sentiments
The analysis confirms that performance diverges dramatically when market emotion is at its peak. The box plot below shows that in "Extreme Greed" scenarios, Top 5% traders have a consistently positive PnL distribution, while Bottom 5% traders suffer significant losses.

!<img width="1400" height="800" alt="advanced_viz_pnl_distribution" src="https://github.com/user-attachments/assets/a4946db0-e42b-4b67-82fc-d5f2c9b378e6" />


### Finding 2: Top Traders Are Superior Risk Managers
Profitability is not just about returns, but about managing risk. The correlation heatmap shows that Total PnL has the strongest positive correlation with the risk-adjusted return metric (`pnl_volatility_ratio`), indicating that top traders generate the most profit **per unit of risk taken**.

<img width="1000" height="700" alt="advanced_viz_correlation_heatmap" src="https://github.com/user-attachments/assets/807ab611-abec-4f2e-a273-a141bf9ec19a" />

### Finding 3: Elite Traders Act as Contrarians Over Time
The time-series analysis reveals a clear behavioral pattern. The performance of Top 5% traders often peaks during or immediately after periods of intense market fear (dips in the grey sentiment line), suggesting they use these moments as buying opportunities.

<img width="1600" height="800" alt="advanced_viz_time_series" src="https://github.com/user-attachments/assets/e4e4b070-8790-451b-bff6-fabb4d6ee87a" />

---

## 6. Technical Requirements & Setup

To run this analysis, you will need Python 3.9+ and the libraries listed in the `requirements.txt` file.

### Installation
1.  Clone the repository:
    ```bash
    git clone [https://github.com/](https://github.com/)[YourUsername]/[YourRepoName].git
    cd [YourRepoName]
    ```
2.  Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

### `requirements.txt`

pandas
numpy
matplotlib
seaborn
scikit-learn

### Conclusion & Recommendations
This project empirically validates the contrarian trading thesis. The data clearly shows that "Smart Money" thrives on volatility by acting against herd mentality, while less successful traders are victimized by it.

### Key Recommendations for Traders:

- Use Sentiment as a Contrarian Indicator: Treat high "Greed" as a signal to reduce risk and high "Fear" as a potential opportunity.

- Prioritize Risk-Adjusted Returns: Focus on consistency and effective risk management, not just chasing large, infrequent wins.

- Systematize Decisions: Develop a clear trading plan to avoid emotional, FOMO-driven decisions, especially during market euphoria.

### Author: Divya Kumar Banjare

LinkedIn: https://www.linkedin.com/in/divyakbanjare/

Email: banjaredivyak@gmail.com
