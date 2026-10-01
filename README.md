# 🌦️ Climate Time-Series Forecasting & Power BI Analytics

An end to end **climate analytics and decision-support project** combining Python based data processing, statistical time-series forecasting, and interactive Power BI dashboards for Sri Lankan meteorological data.

The project uses **NOAA Global Surface Summary of the Day (GSOD)** observations from **2015–2024** to explore climate patterns and generate short term temperature forecasts using **SARIMA** models.

## 🎯 Project Overview

Climate datasets contain strong seasonal patterns, spatial variability, and missing observations, making them difficult to interpret directly.

This project develops an integrated analytical workflow that combines:

- Python based data preprocessing and transformation
- Exploratory and seasonal climate analysis
- Station level and spatial comparisons
- Rainfall variability and extreme-event analysis
- SARIMA time-series forecasting
- Hold-out forecast validation
- Temperature projections with 95% confidence intervals
- Interactive Power BI dashboards for decision support

The objective is to bridge the gap between **statistical forecasting** and **interactive Business Intelligence**, allowing analytical results to be explored without rerunning the underlying models.

## 🧩 Analytical Workflow

```text
NOAA GSOD Data
      ↓
Python Preprocessing
(Cleaning, Unit Conversion, Aggregation)
      ↓
Exploratory & Seasonal Analysis
      ↓
SARIMA Modeling & Validation
      ↓
Forecast Outputs
      ↓
Interactive Power BI Dashboards
```

## 📂 Dataset

Meteorological observations were obtained from the **NOAA Global Surface Summary of the Day (GSOD)** dataset.

**Study period:** January 2015 – December 2024

The analysis includes six Sri Lankan meteorological stations representing coastal, inland, and highland climatic conditions:

- Batticaloa
- Colombo
- Galle
- Jaffna
- Kandy
- Nuwara Eliya

Variables used include mean temperature, maximum and minimum temperature, precipitation, rainy days, and station metadata such as latitude, longitude, and elevation.

Daily observations were cleaned and converted to metric units before being aggregated to monthly resolution.

## 🔬 Methodology

### Data Preprocessing

Python and Pandas were used to standardize dates, select relevant meteorological variables, handle official GSOD missing-value codes, convert measurements to metric units, and aggregate daily observations into monthly indicators.

Missing daily observations were excluded from monthly calculations rather than artificially imputed.

### Exploratory Climate Analysis

The analysis investigates:

- Long-term temperature trends
- Seasonal temperature cycles
- Interannual variability
- Geographic differences between stations
- Rainfall distribution and variability
- Rainfall intensity-frequency relationships

### 📈 SARIMA Forecasting

Seasonal Autoregressive Integrated Moving Average (**SARIMA**) models were used for monthly mean-temperature forecasting.

Models were developed at:

- 🇱🇰 National level
- 📍 Individual station level

A seasonal period of **12 months** was used to represent annual climatic cycles.

### Model Validation

A hold-out validation strategy was used:

| Dataset    | Period                       |
| ---------- | ---------------------------- |
| Training   | January 2015 – December 2022 |
| Validation | January 2023 – December 2024 |
| Forecast   | January 2025 – June 2026     |

Forecast performance was evaluated using **Root Mean Square Error (RMSE)** and **Mean Absolute Error (MAE)**.

## 🏆 National Forecasting Results

The national SARIMA model achieved:

| Metric   |       Result |
| -------- | -----------: |
| **RMSE** | **0.832 °C** |
| **MAE**  | **0.748 °C** |

The average forecast deviation remained below **1°C** during the hold-out validation period.

## 📍 Station-Level Results

| Station      | RMSE (°C) | MAE (°C) |
| ------------ | --------: | -------: |
| Batticaloa   |     1.235 |    0.878 |
| Colombo      |     0.526 |    0.396 |
| Galle        |     0.839 |    0.703 |
| Jaffna       |     1.167 |    0.800 |
| Kandy        |     1.620 |    1.465 |
| Nuwara Eliya |     0.952 |    0.758 |

The results demonstrate spatial variation in forecasting performance across different climatic regions.

## 📊 Power BI Decision-Support Dashboards

Forecasting outputs and processed climate datasets were integrated into **Power BI** to create interactive analytical dashboards.

The dashboards support:

- Temperature trend exploration
- Station-level and spatial analysis
- Rainfall variability analysis
- Year and station filtering
- Historical vs forecast temperature comparison
- Forecast trajectories
- 95% confidence interval visualization

Power BI is used for visualization and interactive exploration, while statistical modeling and validation are performed externally in Python.

## 💡 Key Findings

The analysis identified:

- Strong annual temperature seasonality across Sri Lankan stations.
- Clear geographic and altitudinal differences in temperature.
- Coastal stations generally show higher temperatures than high-elevation locations.
- Nuwara Eliya maintains substantially lower mean temperatures due to elevation.
- Rainfall shows considerably greater variability than temperature.
- Rainfall dispersion increases during late monsoon months, particularly October and November.
- SARIMA captures the recurring seasonal structure of monthly temperature data.
- Forecast accuracy varies across stations, reflecting localized climatic characteristics.

## 🛠️ Technologies & Skills

`Python` • `Pandas` • `Time-Series Analysis` • `SARIMA` • `Statsmodels` • `Forecasting` • `Data Preprocessing` • `Exploratory Data Analysis` • `Power BI` • `Business Intelligence` • `Data Visualization` • `Climate Analytics` • `NOAA GSOD`

<!-- ## 📁 Suggested Repository Structure

```text
Climate-Time-Series-Forecasting-PowerBI/
│
├── README.md
├── notebooks/
│   └── climate_time_series_forecasting.ipynb
├── powerbi/
│   └── climate_analytics_dashboard.pbix
├── results/
│   └── dashboard-screenshots/
├── paper/
│   └── climate_analytics_paper.pdf
├── data/
│   └── README.md
└── requirements.txt
```

> Repository filenames may differ from this suggested structure depending on the uploaded project files.

## 🚀 Running the Analysis

The Python analysis can be opened and executed using **Google Colab** or a local Jupyter environment.

When running locally, install the dependencies required by the notebook and execute the cells sequentially to reproduce the preprocessing, exploratory analysis, validation, and forecasting workflow.

## 📄 Research Paper

**Integrated BI Driven Climate Analytics: Time-Series Forecasting and Interactive Decision Support Dashboards for Sri Lanka**

**Author:** Noorul Ameen Packirdeen Fathima Rizmiya
**Affiliations:** NIBM, Sri Lanka / Ural Federal University, Russia

The accompanying paper documents the methodology, validation results, climate analysis, and integration of statistical forecasting with Power BI.

## 🔭 Future Work

Potential extensions include:

- Multivariable climate forecasting
- Nonlinear rainfall forecasting approaches
- Real-time meteorological data integration
- Extended climate indicators
- Enhanced operational climate-intelligence dashboards

## 👩‍💻 Author

**Noorul Ameen Packirdeen Fathima Rizmiya**

Interests: Artificial Intelligence • Machine Learning • Data Science • Business Intelligence • Data Analytics

--- -->

⭐ If you find this project useful or interesting, consider starring the repository.
