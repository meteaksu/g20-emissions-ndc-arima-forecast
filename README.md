# G20 Sovereign CO2 Emissions Analysis & 2030 Paris NDC Target Forecasting

## 📌 Executive Summary
This project delivers a data-driven policy analytics framework evaluating historical $CO_2$ emission trajectories (1990–2024) across 5 major G20 economies (China, USA, Germany, India, and Turkey). Utilizing an in-memory SQL pipeline and time-series econometrics, the study quantifies absolute target deviations from 2030 Paris Agreement Nationally Determined Contributions (NDCs) and forecasts Germany's 2030 emission trajectory.

---

## 🛠️ Tech Stack & Methodology
* **Core Engine:** Python (`pandas`, `matplotlib`, `statsmodels`)
* **In-Memory SQL Analytics:** `DuckDB` using Advanced Window Functions (`LAG`, `PARTITION BY`, conditional `CASE WHEN` logic)
* **Econometric Modeling:** $ARIMA(1,1,1)$ Time-Series Forecasting
* **Data Standard:** Open World in Data (OWID) CO2 Dataset

---

## 📊 Key Findings
* **Cross-Country Trajectories:** Identified structural emission trends and quantified 2023 cross-sectional deviations from sovereign 2030 NDC targets.
* **Germany Policy Gap Analysis:** The $ARIMA(1,1,1)$ model projects Germany's 2030 emission baseline at **496.64 Mt CO2**, mathematically proving a **46.64 Mt policy gap** against its **450.00 Mt** NDC commitment.

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/meteaksu/g20-emissions-ndc-arima-forecast.git](https://github.com/meteaksu/g20-emissions-ndc-arima-forecast.git)
   pip install pandas matplotlib statsmodels duckdb
