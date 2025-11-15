README — Air Quality Prediction & Analysis (Delhi)
1. Selected Option

I selected Option 2 — AQI & PM2.5 Prediction for Delhi
(using the city_day.csv dataset from the Kaggle dataset “Air Quality Data in India”).

2. Methods and Models Used
Data Loading

Dataset loaded using kagglehub.dataset_download() (no kaggle.json required).

Loaded city_day.csv into a DataFrame of shape (29531, 16).

Initial Filtering & Cleaning

Filtered the dataset for Delhi, resulting in 2009 rows.

Converted 'Date' column to datetime format.

Identified missing values for:

PM2.5, PM10, NO, NO2, NH3, SO2, O3, Xylene, AQI, AQI_Bucket, etc.

Imputed:

Numerical columns → median

AQI_Bucket → mode

Final cleaned dataset had 0 missing values.

Feature Engineering

Set 'Date' as index for time-series operations.

Created lag features (1-day, 2-day, 3-day) for 12 pollutants → 36 new features.

Created target variable:

PM2.5_target = PM2.5.shift(-1)


(next day prediction)

Final modeling dataset:

2005 rows

52 columns (51 features + target)

Train/Test Split

Time-series chronological split (80/20):

Training samples: 1604

Testing samples: 401

Model Used

RandomForestRegressor
Parameters:

RandomForestRegressor(n_estimators=100, random_state=42)


Dropped non-numeric features (City, AQI_Bucket) to avoid errors.

3. Results
Model Performance
Metric	Score
MAE	23.820
RMSE	38.596
R² Score	0.768

This indicates the model explains 76.8% of the variance in PM2.5 levels — strong for environmental time-series data.

Prediction for Next Day

Last date in dataset: 2020-06-30

Predicted PM2.5 for 2020-07-01:

📌 Predicted PM2.5: 45.131
Correlation Insight (for Dashboard)

Top pollutant correlations with PM2.5 (Delhi):

Pollutant	Correlation
PM10	0.848
Benzene	0.697
NO	0.668
NO2	0.648
NH3	0.586
Key Insight

PM10 is the pollutant most strongly correlated with PM2.5 in Delhi, suggesting strong co-emission sources and shared atmospheric behaviors.

A bar chart was created for dashboard integration visualizing these correlations.

4. Summary

This project successfully:

Loaded and cleaned Indian air quality data

Prepared a time-series feature set with lags

Built a RandomForest model to predict next-day PM2.5

Achieved solid evaluation performance

Identified PM10 as the key co-pollutant

Produced a prediction for the next day (July 1, 2020)

The dataset and model pipeline are fully prepared for integration into an air quality forecasting dashboard.
