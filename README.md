# 🌍 Climate Change Forecasting using LSTM Networks

This project leverages deep learning techniques, specifically Long Short-Term Memory (LSTM) networks, to model and forecast critical climate indicators such as global temperature, CO₂ emissions, sea level rise, and extreme weather events. The goal is to understand trends and make projections that support climate awareness and policy-making.

---

## 📌 Project Objectives

- Explore historical climate data and identify significant patterns.
- Preprocess and engineer features suitable for time series forecasting.
- Train LSTM models to capture temporal dependencies.
- Evaluate model performance using appropriate metrics.
- Project future climate trends based on historical patterns.

---

## 🗂 Dataset

The dataset includes time series data for:

- **Global Surface Temperature**
- **Atmospheric CO₂ Emissions**
- **Sea Level Rise**
- **Frequency of Extreme Weather Events**

Data sources are aggregated from publicly available repositories such as:
- [NASA GISTEMP](https://data.giss.nasa.gov/gistemp/)
- [Our World in Data](https://ourworldindata.org/)
- [NOAA Climate Data](https://www.ncei.noaa.gov/)

---

## 🔍 Methodology

### 1. Data Exploration
- Performed visual analysis with line plots and histograms.
- Examined statistical properties and correlations among variables.
- Detected outliers and missing values.

### 2. Preprocessing
- Handled missing values using interpolation.
- Normalized data using MinMaxScaler for model stability.
- Reshaped sequences to 3D format for LSTM: `(samples, time steps, features)`.

### 3. Feature Engineering
- Created lag features and rolling statistics.
- Engineered time-based features like year, decade.
- Aggregated event-based features to monthly/yearly scale.

### 4. LSTM Model Training
- Built and tuned LSTM networks using TensorFlow/Keras.
- Applied `GridSearchCV` for hyperparameter optimization:
  - Epochs
  - Batch size
  - Number of LSTM layers/units
- Used `TimeSeriesSplit` for cross-validation to prevent data leakage.

### 5. Evaluation
- For regression tasks (temperature, CO₂, sea level):
  - Metrics: **MSE**, **RMSE**, **MAE**, and **R²**
- For classification tasks (extreme events):
  - Metrics: **Confusion Matrix**, **Precision**, **Recall**, **F1-Score**
- Compared predicted vs actual values with plots.

### 6. Projections
- Forecasted climate indicators for the next 20–50 years.
- Visualized long-term climate trends.
- Assessed model confidence and uncertainty.

---

## 📈 Results

- The LSTM model accurately captured trends in global temperature and CO₂ levels.
- Sea level projections aligned with observed acceleration trends.
- Model showed potential for early warnings on extreme weather events.

---

## 💡 Key Insights

- Strong correlation between rising CO₂ levels and global temperature.
- Sea level rise shows lagged but exponential growth pattern.
- Climate indicators demonstrate seasonality and long-term upward trends.

---

## 🧪 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/climate-lstm-forecast.git
   cd climate-lstm-forecast
