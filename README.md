# 🚲 Bike Sharing Demand – EDA & Regression Modeling

This project explores and models a bike sharing dataset with the goal of understanding the factors that influence daily rental counts. The notebook walks through a full data science workflow including data cleaning, exploratory data analysis (EDA), feature engineering, and regression modeling.

---

## 📌 Project Motivation

Urban mobility is a growing challenge in modern cities. Understanding patterns in bike-sharing demand can help optimize fleet availability, guide infrastructure development, and improve sustainability efforts. This project aims to analyze real-world bike rental data and predict future demand based on environmental and calendar features.

---

## 🔍 Dataset Overview

- **Observations:** 731 daily records
- **Target Variable:** `rentals` – total number of bikes rented per day
- **Features:** 
  - Numeric: temperature, humidity, windspeed
  - Categorical: season, month, holiday, weekday, weather conditions

---

## 📊 Exploratory Data Analysis (EDA)

1. **Initial Inspection**
   - Null check, datatypes, basic summary statistics

2. **Target Variable Analysis**
   - Distribution plot
   - Boxplots to identify outliers

3. **Temporal Trends**
   - Line plots showing seasonality and yearly comparisons

4. **Numerical Features**
   - Correlation matrix
   - Scatterplots and feature transformations
   - Engineered `difference_temp` to handle collinearity

5. **Categorical Features**
   - Grouped bar charts and violin plots for season, weekday, holiday, and weather

---

## 🤖 Modeling Overview

The following regression models were trained to predict daily rentals:

- **Simple Linear Regression**
  - Based on temperature only
  - Fast and interpretable, but limited in power

- **Polynomial Regression**
  - Applied with `GridSearchCV` to optimize polynomial degree
  - Captures non-linear relationships

- **ElasticNet Regression**
  - Combines L1 and L2 regularization
  - Integrated in a full preprocessing pipeline (numerical + categorical)

### 🧪 Evaluation Metrics

Models were evaluated using:

- R² (coefficient of determination)
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- MAPE (Mean Absolute Percentage Error)

---

## 📈 Visualizations

- Daily rental trends over time
- Correlation matrix and scatter plots
- Residual plots and prediction fit lines
- Histograms of residuals

---

## 💡 Final Insights

- Summer and weekdays show the highest rental demand.
- Temperature is the strongest single predictor.
- Regularized regression with full preprocessing achieved the best performance.
- Simple models are useful for quick estimates but miss non-linear patterns.

---

## 🧭 Recommendations

- Optimize fleet availability based on weather and calendar forecasts.
- Use temperature and seasonality trends to predict peak usage.
- Consider advanced time-series models for finer-grained forecasting.

---

## 🔮 Next Steps

- Incorporate weather forecast data (e.g., rain, humidity predictions)
- Test time-series models like Prophet or ARIMA
- Deploy the best model as a REST API for real-time predictions

---

## 🗂️ Files

- `bike_share_eda.ipynb` – full notebook with analysis and models
- `daily-bike-share.csv` – dataset
- `README.md` – project description
