# 🛒 Walmart Sales Forecasting

A comprehensive machine learning project for predicting weekly sales across Walmart stores and departments using time series analysis and regression modeling.

## 📊 Project Overview

This project tackles the challenge of forecasting retail sales by analyzing historical Walmart sales data combined with external factors like holidays, temperature, fuel prices, and promotional markdowns. The solution implements multiple machine learning models to predict future sales with high accuracy.

## 🎯 Objectives

- Predict weekly sales for 45 Walmart stores across 99 departments
- Analyze seasonal patterns and trends in retail sales
- Evaluate impact of external factors (holidays, promotions, economic indicators)
- Compare performance of different regression algorithms
- Generate actionable insights for retail decision-making

## 📁 Dataset

**Source**: Walmart Sales Forecast (Kaggle)

**Files Used**:
- `train.csv` - Historical sales data (421,570 records)
- `test.csv` - Future periods for prediction (115,064 records)
- `features.csv` - External factors (temperature, fuel price, CPI, unemployment)
- `stores.csv` - Store metadata (type, size)

**Time Period**: 2010-2012 (training) + 2012-2013 (prediction)

## 🔧 Features & Engineering

### Time-Based Features
- Year, Quarter, Month, Week, Day of Year
- Cyclical encoding (sin/cos transformations)
- Holiday indicators and seasonal patterns

### Lag Features
- Sales lag values: 1, 2, 4, 8, 12 weeks
- Rolling averages and standard deviations (4, 8, 12 week windows)

### External Factors
- Temperature, Fuel Price, CPI, Unemployment Rate
- Promotional markdowns (MarkDown1-5)
- Store characteristics (Type A/B/C, Size)

### Derived Features
- Total promotional intensity
- Store-Department combinations
- Holiday vs non-holiday patterns

## 🤖 Models Implemented

1. **Linear Regression** - Baseline model
2. **Random Forest** - Ensemble method with hyperparameter tuning
3. **XGBoost** - Gradient boosting with advanced optimization
4. **LightGBM** - Fast gradient boosting framework

All models include:
- Randomized hyperparameter search (20 iterations)
- 3-fold cross-validation
- Time-aware data splitting (80-20)

## 📈 Results

### Model Performance (R² Score)
- **Linear Regression**: Baseline performance
- **Random Forest**: Enhanced accuracy with ensemble learning
- **XGBoost**: Top-tier performance with gradient boosting
- **LightGBM**: Optimal speed-accuracy balance

### Key Insights
- Seasonal patterns significantly impact sales
- Promotional markdowns drive sales increases
- Store type and department combination are critical factors
- External economic factors show moderate influence

## 🛠️ Technologies Used

- **Python 3.x**
- **Data Processing**: Pandas, NumPy
- **Machine Learning**: Scikit-learn, XGBoost, LightGBM
- **Time Series**: Statsmodels
- **Visualization**: Matplotlib, Seaborn
- **Statistics**: SciPy

## 📊 Visualizations

- Time series plots showing sales trends
- Seasonal decomposition analysis
- Actual vs Predicted comparisons
- Feature importance rankings
- Sales distribution by store type and department

## 🚀 Usage

1. **Setup Environment**:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm statsmodels scipy
```

2. **Run the Analysis**:
```bash
python time_series.py
```

3. **Output**:
- Model performance metrics
- Visualizations and plots
- `walmart_sales_predictions.csv` - Future sales predictions

## 🔍 Key Findings

1. **Seasonality**: Strong seasonal patterns with peaks during holidays
2. **Promotions**: MarkDown events significantly boost sales
3. **Store Types**: Type A stores consistently outperform B and C
4. **Department Variation**: High variance in performance across departments
5. **External Factors**: Economic indicators show moderate predictive power

## 🎓 Learning Outcomes

- Time series forecasting techniques
- Feature engineering for retail data
- Hyperparameter optimization strategies
- Model comparison and selection
- Business insights from data analysis

## 🤝 Contributing

This project was developed as part of an internship with Elevvo Pathways. Suggestions and improvements are welcome!

---
