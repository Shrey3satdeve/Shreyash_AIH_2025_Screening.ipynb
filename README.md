🌫️ Air Quality Prediction & Analysis (Delhi)

Forecasting PM2.5 levels using Machine Learning + Time-Series Features

<p align="center"> <img src="assets/air_quality_banner.png" alt="Air Quality Banner" width="85%"> </p>
🚀 Badges
<p align="left"> <img src="https://img.shields.io/badge/Python-3.10-blue" /> <img src="https://img.shields.io/badge/Machine%20Learning-RandomForest-green" /> <img src="https://img.shields.io/badge/TimeSeries-Enabled-orange" /> <img src="https://img.shields.io/badge/Data%20Source-Kaggle-blueviolet" /> <img src="https://img.shields.io/badge/Status-Completed-brightgreen" /> <img src="https://img.shields.io/badge/Forecast-PM2.5-red" /> </p>
🧭 1. Selected Option

I selected Option 2 → Next-Day PM2.5 Prediction for Delhi using the
city_day.csv dataset from Kaggle (Air Quality Data in India).

📂 2. Data Loading

Loaded dataset via:

kagglehub.dataset_download('rohanrao/air-quality-data-in-india', 'city_day.csv')


📌 Dataset Shape: 29,531 rows × 16 columns

🧹 3. Data Cleaning
✔ Filtered for Delhi → 2,009 rows
✔ Converted 'Date' to datetime
✔ Handled Missing Values

Numerical columns → median

AQI_Bucket → mode

All missing values successfully filled.

✨ Final clean dataset → 0 missing values
⚙️ 4. Feature Engineering
✔ Set Date as index
✔ Created lag features for 12 pollutants:

Lag 1, 2, 3 → total 36 engineered features

✔ Defined prediction target:
df_delhi['PM2.5_target'] = df_delhi['PM2.5'].shift(-1)

📦 Final Modeling Dataset:

2005 samples

51 features + 1 target = 52 columns

✂️ 5. Train/Test Split

Performed 80/20 chronological split to preserve time order:

Split	Samples
Train	1,604
Test	401


🤖 6. Model Used
RandomForestRegressor
RandomForestRegressor(n_estimators=100, random_state=42)


Dropped non-numeric features:

['City', 'AQI_Bucket']

📈 7. Model Performance
Metric	Score
MAE	23.820
RMSE	38.596
R²	0.768

✔ Explains 76.8% of PM2.5 variance
✔ Stable & reliable model for air-quality forecasting

🔮 8. Next-Day Prediction

📅 Last date in data: 2020-06-30
🌤️ Predicted PM2.5 for 2020-07-01:

👉 45.131
📊 9. Pollutant Correlation Analysis

Correlation with PM2.5:

Pollutant	Correlation
PM10	0.848
Benzene	0.697
NO	0.668
NO2	0.648
NH3	0.586
🔍 Key Insight

PM10 is the strongest predictor of PM2.5

Both pollutants share common emission sources.


📝 10. Summary

This project successfully:

✔ Loaded and cleaned Indian air-quality data
✔ Generated lag features for time-series prediction
✔ Built a RandomForest model predicting next-day PM2.5
✔ Achieved strong metrics (R² = 0.768)
✔ Identified PM10 as the strongest co-pollutant
✔ Forecasted PM2.5 for 2020-07-01: 45.131
✔ Prepared visualizations for dashboard integration
