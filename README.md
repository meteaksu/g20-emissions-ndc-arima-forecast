# G20 CO₂ Trajectory Analysis, NDC Target Benchmarking & Econometric Forecasting

## Executive Summary
This project evaluates national decarbonization trajectories across G20 economies with a targeted econometric deep-dive into Germany’s climate mitigation pathways. By pairing historical CO₂ emissions data with official Paris Agreement **Nationally Determined Contributions (NDCs)**, this study benchmarks actual policy targets against empirical projections. Utilizing an **ARIMA(0,1,0) with Drift** model, the analysis identifies a projected **37.2 Mt CO₂ policy gap** for Germany by 2030, highlighting structural shortfalls in current decarbonization rates.

---

## Key Features & Technical Highlights

* **SQL & Window Functions (`DuckDB`):** Processed multi-decadal historical emissions data and calculated year-over-year percentage changes using advanced windowing (`LAG()`).
* **Stationarity & Econometric Rigor:** Applied the **Augmented Dickey-Fuller (ADF) test** to verify non-stationarity in levels and established first-difference stationarity ($I(1)$ process).
* **Model Selection & Forecasting (`statsmodels`):** Evaluated candidate ARIMA models based on Akaike Information Criterion (AIC) minimization, identifying an **ARIMA(0,1,0) with Drift** as the optimal specification for capturing persistent downward deterministic trends.
* **Policy Gap Quantization:** Computed the empirical divergence between the 2030 ARIMA forecast trajectory and Germany's binding NDC target ($65\%$ reduction relative to 1990 levels).

---

## Analytical Pipeline Workflow

[ Raw G20 CO₂ Emissions Data ]
│
▼
[ DuckDB Window Functions ] ──► (YoY Growth Rates & Lag Computations)
│
▼
[ Econometric Testing ] ────► (ADF Unit-Root Testing & First-Differencing)
│
▼
[ ARIMA Modeling (0,1,0) ] ──► (Drift Estimation via statsmodels)
│
▼
[ Policy Gap Benchmarking ] ──► (2030 Forecast vs. Official NDC Target)
│
▼
[ Matplotlib Trajectory Map ] ──► (Publication-ready Policy Visualization)

---

## Key Results & Econometric Metrics

| Metric / Parameter | Value | Economic / Statistical Interpretation |
| :--- | :--- | :--- |
| **Historical Base Year (1990)** | 1,250 Mt CO₂ | Benchmark reference level for EU/German NDC targets |
| **2030 NDC Target (-65%)** | 437.5 Mt CO₂ | Statutory 2030 emission cap under German Climate Action Act |
| **2030 ARIMA Forecast** | 474.7 Mt CO₂ | Empirical point forecast based on historical drift rate |
| **Projected Policy Gap** | **+37.2 Mt CO₂** | Identified policy gap requiring accelerated structural reform |
| **ADF Test (1st Difference)** | $p < 0.05$ | Confirmed unit-root elimination / stationarity achieved |

---

## Tech Stack & Dependencies

* **Language:** Python 3.x
* **Data Processing & SQL:** `duckdb`, `pandas`, `numpy`
* **Econometrics & Time Series:** `statsmodels`
* **Visualization:** `matplotlib`

---

## How to Run

   Clone the repository:
   ```bash
   git clone (https://github.com/meteaksu/g20-emissions-ndc-arima-forecast.git)
   cd g20-emissions-ndc-arima-forecast

   Install required packages:
   pip install pandas numpy duckdb statsmodels matplotlib

   Execute the Jupyter Notebook:
   jupyter notebook project.ipynb



   
