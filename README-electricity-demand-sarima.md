# ⚡ Electricity Demand Forecasting with SARIMA

## 📌 Business Problem
The organization responsible for overseeing electricity generation and distribution in **California** needs to ensure efficient operations by aligning energy supply with expected demand.

Poor demand estimation can have significant consequences:

- **Overestimation:**
  - Excess energy production
  - Costs from storage or wasted resources

- **Underestimation:**
  - Power supply failures
  - Negative impact on residential and industrial customers

An accurate forecasting model is therefore key to optimizing costs, improving operational efficiency, and guaranteeing service stability.

---

## 🎯 Analysis Objectives

### Main objective
Develop a time series model capable of forecasting hourly electricity demand in California over a short-term horizon of up to **24 hours**.

### Specific objectives
- Analyze the historical behavior of energy demand
- Identify trend and seasonality patterns
- Prepare a clean, consistent time series
- Assess stationarity using statistical tests
- Build a baseline model for comparison
- Implement a **SARIMA** model to improve forecast accuracy
- Evaluate the model using metrics such as **RMSE** and **MAPE**
- Analyze residuals to validate model quality

---

## 📊 Data Used
The analysis uses real hourly electricity demand data from the state of **California, United States**.

Key characteristics:
- **Time variable:** `period`
- **Target variable:** `value` (energy demand)
- **Original granularity:** energy sub-regions (`subba`)
- **Transformation:** aggregation by timestamp to obtain a single statewide time series

Processing performed:
- Conversion of dates to `datetime` format
- Chronological sorting
- Identification of missing values
- Linear interpolation of missing data
- Outlier detection and treatment using the **Tukey method**

---

## ⚙️ Technologies & Libraries

### Technologies
- Python
- Jupyter Notebook

### Libraries
- **pandas** → data manipulation and transformation
- **numpy** → numerical operations
- **matplotlib** → data visualization
- **seaborn** → exploratory analysis
- **statsmodels** → series decomposition, ACF/PACF, ADF test, and SARIMA/SARIMAX modeling
- **scikit-learn** → model evaluation metrics

---

## 📁 Main File
**`pronostico_demanda_electricidad_sarima.ipynb`**

Contains the complete project workflow:
- Data loading and cleaning
- Exploratory data analysis
- Seasonality identification
- Baseline modeling
- SARIMA implementation
- Evaluation and residual analysis

---

## 🔍 Technical Findings
- A clear **daily seasonality (24 hours)** was identified.
- The SARIMA model outperformed the baseline model.
- Residuals show a slight overestimation, indicating room for improvement.

---

## 💡 Business Impact
Accurate energy demand estimation is critical to operations. Improving forecast precision makes it possible to:

- Reduce operating costs
- Increase energy efficiency
- Guarantee supply stability

---

## 🔮 Future Improvements
- Incorporate exogenous variables (temperature, holidays, day type)
- Optimize the model's hyperparameters
- Evaluate alternative models (Prophet, XGBoost, LSTM)

---
