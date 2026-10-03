# Energy Demand Forecasting Using ARIMA

A time-series forecasting project using hourly Italian electricity load and solar generation data from 2016. The notebook performs data cleaning, stationarity testing, ACF/PACF analysis, chronological train/test splitting, ARIMA modelling, and RMSE evaluation.

## Project Objectives
- Analyze hourly electricity demand and solar generation.
- Check and handle missing values.
- Test stationarity using the Augmented Dickey-Fuller (ADF) test.
- Explore autocorrelation using ACF and PACF.
- Build ARIMA forecasting models.
- Evaluate forecasts using RMSE.

## Dataset
The dataset contains 8,784 hourly observations for Italy in 2016.

| Column | Description |
|---|---|
| `utc_timestamp` | UTC timestamp |
| `IT_load_new` | Electricity load/demand |
| `IT_solar_generation` | Solar generation |

## Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn
- Jupyter Notebook

## Methodology
1. Load the dataset.
2. Inspect and visualize the time series.
3. Detect missing values.
4. Forward-fill missing load values.
5. Convert timestamps to datetime.
6. Perform ADF stationarity testing.
7. Inspect ACF and PACF plots.
8. Split the data chronologically into training and testing sets.
9. Fit ARIMA models.
10. Generate forecasts and calculate RMSE.

## Models
The notebook evaluates ARIMA configurations including:
- ARIMA(2,0,2)
- ARIMA(2,1,2)
- ARIMA(2,2,2)

The ARIMA(2,2,2) implementation has been corrected in this GitHub version so that the `(2,2,2)` model is actually fitted before forecasting.

## Evaluation
The primary evaluation metric is Root Mean Squared Error (RMSE). The original notebook reported an RMSE of approximately 7714.95 for the load ARIMA(2,0,2) model. Results can vary slightly with library versions or code changes.

## Project Structure
```text
Energy-Demand-Forecasting-ARIMA/
├── data/
│   └── TimeSeries_TotalSolarGen_and_Load_IT_2016.csv
├── notebooks/
│   └── Energy_Demand_Forecasting_using_ARIMA.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run
```bash
git clone <your-repository-url>
cd Energy-Demand-Forecasting-ARIMA
pip install -r requirements.txt
jupyter notebook
```
Open the notebook in `notebooks/` and run the cells.

## Future Improvements
- Use SARIMA/SARIMAX to model strong hourly seasonality.
- Perform systematic hyperparameter selection using AIC/BIC and time-series validation.
- Add exogenous variables such as solar generation, weather, and calendar features.
- Compare ARIMA against Prophet, XGBoost, LightGBM, and LSTM models.
- Build a small dashboard or web application for interactive forecasting.

## Author
**Pranit Sadaphal**

Artificial Intelligence & Data Science Student | Data Science & Machine Learning
