
# Bike Sharing Demand Analysis

This project presents a full **Exploratory Data Analysis (EDA)** of the *Daily Bike Share* dataset. The goal of the analysis is to understand factors influencing bike rentals and prepare the dataset for further machine learning modeling.

---

## Dataset Overview

The dataset includes daily historical data from a bike-sharing company, containing:

- **731 records**
- **14 features**, including:
  - Weather conditions (temperature, humidity, windspeed)
  - Date-related features (season, month, weekday, holiday)
  - Target variable: `rentals` (number of bikes rented daily)

Data source: *daily-bike-share.csv*

---

## Technologies Used

- **Python 3**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## EDA Process

1. **Data Loading & Cleaning**
   - Converted date fields to datetime format.
   - Removed non-informative features (e.g., row ID, year).

2. **Target Variable Analysis**
   - Rentals are highly skewed.
   - High variance between daily rentals.

3. **Time-Series Exploration**
   - Weekly seasonality detected.
   - Rentals peak during summer months.

4. **Numerical Feature Analysis**
   - Strong correlation between temperature and rentals.
   - Negative correlation for humidity and windspeed.
   - Engineered a new feature: `difference_temp` to capture variance between temperature and "feels like" temperature.

5. **Categorical Feature Analysis**
   - Analyzed categorical variables using violin plots.
   - Seasonality, holidays, and weekdays show significant impact on demand.

---

## Key Insights

- **Temperature** is the most important factor for bike rentals.
- **Summer months and working days** show higher rental volumes.
- **Bad weather conditions (rain, snow, high humidity, high windspeed)** lead to lower rentals.
- Weekly seasonality pattern is visible due to different behavior on weekends vs weekdays.
- Additional feature engineering improved data quality for modeling.

---

## How to Run

1. Clone the repository or download the project files.
2. Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

3. Open the notebook file in Jupyter:

```bash
jupyter notebook bike_share_eda_professional.ipynb
```

4. Run all cells to reproduce the analysis.

---

## Project Status

✅ Data exploration and feature engineering completed  
🚀 Ready for model development (regression, time-series forecasting, etc.)

---
