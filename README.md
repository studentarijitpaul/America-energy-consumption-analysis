#  Time Series Forecasting using XGBoost

A machine learning project that forecasts hourly electricity demand using the AEP (American Electric Power) energy consumption dataset. The project demonstrates feature engineering for time series data and builds a forecasting model using XGBoost Regression.

---

##  Project Overview

Time series forecasting plays an important role in industries such as:

 Energy Demand Forecasting
   Sales Prediction
   Weather Forecasting
   Financial Market Analysis
   Industrial Resource Planning

In this project, an **XGBoost Regressor** is trained on historical electricity consumption data to predict future energy demand.

---

## Dataset

**Dataset:** `AEP_hourly.csv`

The dataset contains:

- Datetime
- Hourly electricity demand (MW)

Target Variable:

- **AEP_MW**

---

##  Project Workflow

### 1. Import Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

### 2. Load Dataset

- Read CSV file
- Convert Datetime column into datetime format
- Set Datetime as index

---

### 3. Exploratory Data Analysis (EDA)

Performed:

- Dataset information
- Shape inspection
- Time series visualization
- Training vs Testing data visualization
- Hour-wise electricity demand analysis
- Month-wise electricity demand analysis

---

### 4. Feature Engineering

Created several time-based features from the Datetime index:

| Feature | Description |
|---------|-------------|
| Hour | Hour of the day |
| Day of Week | Monday–Sunday |
| Quarter | Quarter of year |
| Month | Month number |
| Year | Year |
| Day of Year | Day number within the year |
| Day of Month | Day number within the month |
| Week of Year | ISO week |

Model Features:

```python
[
'dayofyear',
'hour',
'dayofweek',
'quarter',
'month',
'year'
]
```

---

### 5. Train-Test Split

Training data:
- Before January 10, 2015

Testing data:
- From January 10, 2015 onward

---

### 6. Model Building

Model Used:

**XGBoost Regressor**

Parameters:

- n_estimators = 1000
- learning_rate = 0.01
- max_depth = 3
- objective = reg:squarederror
- early_stopping_rounds = 50
- random_state = 42

---

### 7. Model Evaluation

Evaluation Metric:

- Root Mean Squared Error (RMSE)

The notebook also identifies:

- Highest prediction errors
- Weekly prediction comparison
- Actual vs Predicted values

---

### 8. Feature Importance

The project visualizes the importance of engineered time-based features used by XGBoost.

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- Jupyter Notebook


---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Time-Series-Forecasting.git
```

Move into the project directory

```bash
cd Time-Series-Forecasting
```

Install dependencies

```bash
pip install -r requirement.txt
```

Run Jupyter Notebook

```bash
jupyter notebook
```

---

##  Results

The model successfully learns seasonal and temporal patterns in electricity consumption using engineered time-based features.

The notebook includes:

- Time series visualization
- Feature engineering
- XGBoost training
- Forecasting
- RMSE evaluation
- Feature importance analysis
- Error analysis

---

##  Future Improvements

- Add lag features
- Rolling window statistics
- Holiday feature engineering
- Hyperparameter tuning with GridSearchCV
- Cross-validation for time series
- Compare with ARIMA, SARIMA, Prophet, and LSTM models
- Deploy using Streamlit or Flask

---
    
##  Author

**Arijit Paul**

Data Science | Machine Learning | AI Enthusiast

If you found this project useful, consider giving it a ⭐ on GitHub.
