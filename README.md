# Time Series Analysis: Wind Power Forecasting

## Project Overview
Achieved a top 3 ranking among 40 groups, this project presents a comprehensive approach to forecasting wind power generation. Utilizing the Prophet model, we accomplished a highly accurate forecast with an RMSE score of 162.88, and identified the optimal seasonal forecasting period.

## Data Cleaning and Preparation
- Loaded data from `train.csv`, focusing on `ActivePower` and `WindSpeed`.
- Performed data aggregation on a daily basis and handled missing values through forward and backward filling.
- Split the data into training and test sets for model validation.

## Visual Analysis
- Conducted time series analysis revealing significant seasonal peaks, particularly in August.
- Decomposed the time series to understand underlying patterns using ACF and PACF plots.

## Model Development and Evaluation
### 1. Prophet
- Customized the Prophet model with yearly seasonality to fit the time series data.
- Achieved a Test RMSE of 162.88, indicating high model accuracy.

### 2. Exponential Smoothing (SES and ES)
- Explored Simple and Exponential Smoothing methods, finding an optimal smoothing level (alpha) of 0.9.
- RMSE for SES and ES models were 177.51 and 178.95 respectively, showing competitive performance.

### 3. LSTM
- Normalized the data and created a dataset with a look-back period of 250 days.
- Developed a Bidirectional LSTM model, resulting in a Test RMSE of 182.60.

### 4. SARIMAX + LSTM (Combined Approach)
- Implemented a SARIMAX model to account for seasonal trends and external factors (WindSpeed).
- Enhanced the SARIMAX predictions with LSTM residuals, yielding the best RMSE of 59.03 but noted potential overfitting.

## Conclusion
Our comprehensive analysis and evaluation of various models led to a nuanced understanding of the wind power generation's time series characteristics. Despite the outstanding performance of the combined SARIMAX and LSTM approach, we eventually selected the Prophet model due to its balance of accuracy and stability, avoiding the overfitting observed in the more complex model. This decision underlines our commitment to developing reliable and practical solutions for forecasting in the renewable energy sector.

