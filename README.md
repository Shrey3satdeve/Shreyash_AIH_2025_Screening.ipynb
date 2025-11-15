# 🌫️ Delhi Air Quality Prediction & Analysis

> **Advanced Machine Learning Pipeline for PM2.5 Forecasting and Environmental Intelligence**

<p align="center">
  <img src="[https://img.shields.io/badge/Python-3.10+-blue.svg?style=for-the-badge&logo=pytho](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.incredibleindia.gov.in%2Fen%2Fdelhi%2Fdelhi%2Findia-gate&psig=AOvVaw2EpykhMXx33w17YQ8aLFTN&ust=1763315218719000&source=images&cd=vfe&opi=89978449&ved=0CBUQjRxqFwoTCPjqupzb9JADFQAAAAAdAAAAABAE)n" alt="Python">
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/github/stars/Shrey3satdeve/Shreyash_AIH_2025_Screening.ipynb?style=for-the-badge" alt="Stars">
  <img src="https://img.shields.io/github/last-commit/Shrey3satdeve/Shreyash_AIH_2025_Screening.ipynb?style=for-the-badge" alt="Last Commit">
  <img src="https://img.shields.io/github/issues/Shrey3satdeve/Shreyash_AIH_2025_Screening.ipynb?style=for-the-badge" alt="Issues">
  <img src="https://img.shields.io/badge/code%20style-black-000000.svg?style=for-the-badge" alt="Code Style">
</p>

<p align="center">
  <img src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Delhi India Gate Air Quality Banner" width="85%">
</p>
<p align="center">
  <em>AI-Powered Air Quality Forecasting for Delhi's Future</em>
</p>

---

## 🚀 Overview

**Delhi Air Quality Prediction** is a comprehensive machine learning solution that forecasts PM2.5 pollution levels using advanced time-series analysis and ensemble methods. Built for environmental scientists, policy makers, and health organizations to make data-driven decisions about air quality management.

### 🎯 Key Features

- **🔮 Next-Day PM2.5 Prediction** - Accurate 24-hour ahead forecasting
- **📊 Multi-Pollutant Analysis** - Correlations between 12+ air quality indicators  
- **⚡ Real-time API** - FastAPI-powered prediction endpoints
- **📈 Interactive Visualizations** - Comprehensive plotting and trend analysis
- **🤖 Production-Ready ML Pipeline** - Automated feature engineering and model training
- **📱 Web Dashboard** - User-friendly interface for predictions and insights

---

## 🏗️ Project Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Data Ingestion │───▶│  Preprocessing   │───▶│ Feature Engineer │
│   (Kaggle API)   │    │   & Cleaning     │    │   (Lag Features) │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   EDA & Analysis │    │  Model Training  │    │   Evaluation     │
│   (Correlations) │    │ (Random Forest)  │    │   & Validation   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Visualization  │    │   API Deployment │    │   Monitoring &   │
│   & Reporting    │    │   (FastAPI)      │    │   Alerting       │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

---

## 📁 Project Structure

```
Delhi-Air-Quality-Prediction/
├── 📂 src/
│   ├── data/
│   │   ├── __init__.py
│   │   ├── loader.py          # Data loading utilities
│   │   └── preprocessor.py    # Data cleaning & preprocessing
│   ├── features/
│   │   ├── __init__.py
│   │   ├── engineering.py     # Feature engineering pipeline
│   │   └── selection.py       # Feature selection methods
│   ├── models/
│   │   ├── __init__.py
│   │   ├── trainer.py         # Model training pipeline
│   │   ├── predictor.py       # Prediction utilities
│   │   └── evaluator.py       # Model evaluation metrics
│   └── utils/
│       ├── __init__.py
│       ├── config.py          # Configuration management
│       └── helpers.py         # Utility functions
├── 📂 notebooks/
│   ├── 01_data_loading.ipynb         # Data exploration & loading
│   ├── 02_preprocessing.ipynb        # Data cleaning & validation
│   ├── 03_feature_engineering.ipynb  # Feature creation & selection
│   ├── 04_model_training.ipynb       # ML model development
│   └── 05_evaluation.ipynb           # Performance analysis
├── 📂 api/
│   ├── __init__.py
│   ├── app.py                 # FastAPI application
│   ├── routes/
│   │   ├── predict.py         # Prediction endpoints
│   │   └── stats.py          # Statistics endpoints
│   └── schemas/
│       └── models.py         # Pydantic models
├── 📂 config/
│   ├── model_config.yaml     # Model hyperparameters
│   ├── data_config.yaml      # Data processing settings
│   └── api_config.yaml       # API configuration
├── 📂 models/
│   ├── random_forest_model.pkl  # Trained model artifacts
│   ├── scaler.pkl              # Feature scaler
│   └── feature_names.pkl       # Feature column names
├── 📂 data/
│   ├── raw/                   # Original datasets
│   ├── processed/             # Cleaned datasets
│   └── external/              # External data sources
├── 📂 plots/
│   ├── pm25_trend.png         # Time series plots
│   ├── correlation_matrix.png  # Feature correlations
│   └── model_performance.png   # Evaluation metrics
├── 📂 tests/
│   ├── test_data.py           # Data processing tests
│   ├── test_models.py         # Model testing
│   └── test_api.py            # API endpoint tests
├── 📄 requirements.txt        # Python dependencies
├── 📄 environment.yml         # Conda environment
├── 📄 Dockerfile            # Container configuration
├── 📄 docker-compose.yml    # Multi-service setup
├── 📄 .gitignore           # Git ignore rules
├── 📄 LICENSE              # MIT License
└── 📄 README.md            # This file
```

---

## 📊 Dataset Description

**Source**: [Air Quality Data in India (Kaggle)](https://www.kaggle.com/rohanrao/air-quality-data-in-india)

| Feature | Description | Data Type |
|---------|-------------|-----------|
| `Date` | Measurement date | datetime |
| `PM2.5` | Fine particulate matter (μg/m³) | float |
| `PM10` | Particulate matter (μg/m³) | float |
| `NO` | Nitric oxide (μg/m³) | float |
| `NO2` | Nitrogen dioxide (μg/m³) | float |
| `NOx` | Nitrogen oxides (ppb) | float |
| `NH3` | Ammonia (μg/m³) | float |
| `CO` | Carbon monoxide (mg/m³) | float |
| `SO2` | Sulfur dioxide (μg/m³) | float |
| `O3` | Ozone (μg/m³) | float |
| `Benzene` | Benzene (μg/m³) | float |
| `Toluene` | Toluene (μg/m³) | float |
| `Xylene` | Xylene (μg/m³) | float |
| `AQI` | Air Quality Index | integer |
| `AQI_Bucket` | AQI category | categorical |

**Dataset Stats**:
- **Total Records**: 29,531 observations
- **Delhi Subset**: 2,009 records
- **Date Range**: 2015-01-01 to 2020-06-30
- **Missing Values**: Handled via median/mode imputation

---

## ⚡ Quick Start

```bash
# Clone the repository
git clone https://github.com/Shrey3satdeve/Shreyash_AIH_2025_Screening.ipynb.git
cd Shreyash_AIH_2025_Screening.ipynb

# Install dependencies
pip install -r requirements.txt

# Run the main pipeline
python src/main.py

# Start the API server
python api/app.py
```

---

## 🛠️ Installation & Setup

### Prerequisites

- Python 3.10+
- pip or conda package manager
- Git

### Environment Setup

#### Option 1: Using pip

```bash
# Create virtual environment
python -m venv venv

# Activate environment
# On Windows
venv\Scripts\activate
# On macOS/Linux  
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

#### Option 2: Using conda

```bash
# Create conda environment
conda env create -f environment.yml

# Activate environment
conda activate air-quality-prediction
```

#### Option 3: Using Docker

```bash
# Build and run with Docker
docker-compose up --build

# Access API at http://localhost:8000
```

---

## 🚀 How to Run

### 1. **Run Jupyter Notebooks**

```bash
# Start Jupyter Lab
jupyter lab

# Execute notebooks in order:
# 01_data_loading.ipynb → 02_preprocessing.ipynb → ... → 05_evaluation.ipynb
```

### 2. **Run Main Pipeline**

```bash
# Execute full ML pipeline
python src/main.py --config config/model_config.yaml

# Train model only
python src/models/trainer.py --data data/processed/delhi_clean.csv

# Generate predictions
python src/models/predictor.py --model models/random_forest_model.pkl
```

### 3. **Start API Server**

```bash
# Launch FastAPI server
python api/app.py

# API will be available at: http://localhost:8000
# Interactive docs: http://localhost:8000/docs
```

---

## 🔌 API Documentation

### Base URL: `http://localhost:8000`

#### **POST /predict**
Get next-day PM2.5 prediction for specific input features.

```bash
curl -X POST "http://localhost:8000/predict" \
  -H "Content-Type: application/json" \
  -d '{
    "PM10": 150.0,
    "NO2": 45.0,
    "Benzene": 2.5,
    "NO": 35.0,
    "NH3": 25.0
  }'
```

**Response:**
```json
{
  "prediction": 45.131,
  "confidence_interval": [38.2, 52.1],
  "risk_level": "Moderate",
  "timestamp": "2025-11-15T17:46:08Z"
}
```

#### **GET /forecast**
Get 7-day PM2.5 forecast.

```bash
curl -X GET "http://localhost:8000/forecast?days=7"
```

#### **GET /stats**
Get pollution statistics and correlations.

```bash
curl -X GET "http://localhost:8000/stats"
```

---

## 🤖 Model Details

### **Algorithm**: Random Forest Regressor

**Why Random Forest?**
- ✅ Handles non-linear relationships
- ✅ Robust to outliers
- ✅ Feature importance ranking
- ✅ No overfitting with proper tuning

### **Hyperparameters**
```yaml
n_estimators: 100
max_depth: 15
min_samples_split: 5
min_samples_leaf: 2
random_state: 42
```

### **Feature Engineering**
- **Lag Features**: 1, 2, 3-day historical values for 12 pollutants (36 features)
- **Temporal Features**: Day of week, month, season
- **Rolling Statistics**: 7-day moving averages
- **Interaction Terms**: PM10×Benzene, NO×NO2

### **Evaluation Metrics**
| Metric | Score | Interpretation |
|--------|-------|----------------|
| **MAE** | 23.82 μg/m³ | Average prediction error |
| **RMSE** | 38.60 μg/m³ | Root mean squared error |
| **R²** | 0.768 | Explains 76.8% of variance |
| **MAPE** | 18.4% | Mean absolute percentage error |

---

## 📈 Visual Outputs

### Time Series Analysis
![PM2.5 Trend Analysis](plots/pm25_trend.png)
*Figure 1: Historical PM2.5 levels in Delhi (2015-2020)*

### Feature Correlations
![Correlation Matrix](plots/correlation_matrix.png)
*Figure 2: Pollutant correlation heatmap*

### Model Performance
![Model Evaluation](plots/model_performance.png)
*Figure 3: Prediction vs actual values with confidence intervals*

### Seasonal Patterns
![Seasonal Analysis](plots/seasonal_patterns.png)
*Figure 4: Monthly and weekly pollution patterns*

### Feature Importance
![Feature Rankings](plots/feature_importance.png)
*Figure 5: Top 15 most important features for prediction*

---

## 📚 Notebook Summary

| Notebook | Purpose | Key Outputs |
|----------|---------|-------------|
| **01_data_loading.ipynb** | Data acquisition and initial exploration | Dataset overview, missing value analysis |
| **02_preprocessing.ipynb** | Data cleaning and validation | Clean dataset, outlier detection |
| **03_feature_engineering.ipynb** | Feature creation and selection | 51 engineered features, correlation analysis |
| **04_model_training.ipynb** | ML model development | Trained Random Forest model |
| **05_evaluation.ipynb** | Performance analysis and visualization | Evaluation metrics, prediction plots |

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|-------------|
| **Language** | Python 3.10+ |
| **ML Framework** | scikit-learn, pandas, numpy |
| **Visualization** | matplotlib, seaborn, plotly |
| **API** | FastAPI, Pydantic, uvicorn |
| **Data** | Kaggle API, CSV processing |
| **Testing** | pytest, unittest |
| **Deployment** | Docker, Docker Compose |
| **Environment** | conda, pip, virtual environments |
| **Code Quality** | black, flake8, pre-commit |

---

## 🚀 Future Improvements

### **Model Enhancements**
- [ ] Deep Learning (LSTM, Transformer) for sequence modeling
- [ ] Ensemble methods (XGBoost + Random Forest)
- [ ] Real-time model retraining pipeline
- [ ] Uncertainty quantification with Bayesian methods

### **Data & Features**
- [ ] Weather data integration (temperature, humidity, wind)
- [ ] Satellite imagery for spatial features  
- [ ] Traffic data correlation analysis
- [ ] Industrial emission source mapping

### **Production Features**
- [ ] Real-time data streaming (Apache Kafka)
- [ ] Model monitoring and drift detection
- [ ] A/B testing framework for model versions
- [ ] Alert system for dangerous pollution levels

### **UI/UX Improvements**
- [ ] Interactive React.js dashboard
- [ ] Mobile app for citizens
- [ ] Email/SMS alert subscriptions
- [ ] Historical data comparison tools

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### **Development Setup**

```bash
# Fork the repository
git clone https://github.com/yourusername/Shreyash_AIH_2025_Screening.ipynb.git

# Create feature branch
git checkout -b feature/amazing-feature

# Install development dependencies
pip install -r requirements-dev.txt

# Run tests
pytest tests/

# Run code quality checks
black src/
flake8 src/

# Commit changes
git commit -m "Add amazing feature"

# Push to branch
git push origin feature/amazing-feature

# Open Pull Request
```

### **Contribution Areas**
- 🐛 Bug fixes and error handling
- 📊 New visualization features
- 🤖 Alternative ML algorithms
- 📱 Frontend development
- 📚 Documentation improvements
- ⚡ Performance optimizations

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Shreyash Satdeve

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## 👨‍💻 Author & Contact

**Shreyash Satdeve**  
🔗 GitHub: [@Shrey3satdeve](https://github.com/Shrey3satdeve)  
📧 Email: [shrey3satdeve@gmail.com](mailto:shrey3satdeve@gmail.com)  
💼 LinkedIn: [Shreyash Satdeve](https://linkedin.com/in/shreyash-satdeve)  

---

## ❓ Frequently Asked Questions

### **Q: How accurate are the predictions?**
A: Our model achieves 76.8% variance explanation (R² = 0.768) with an average error of 23.82 μg/m³, which is competitive for air quality forecasting.

### **Q: Can I use this for other cities?**
A: Yes! The pipeline is designed to be city-agnostic. Simply replace the dataset with data from your target city and retrain the model.

### **Q: How often should the model be retrained?**
A: We recommend retraining monthly with new data to maintain accuracy, or when model drift is detected.

### **Q: What's the minimum data requirement?**
A: At least 1 year of daily air quality data is recommended for reliable model training.

### **Q: Does this work for real-time predictions?**
A: Yes, the API supports real-time predictions. Connect it to live data feeds for continuous forecasting.

### **Q: How can I add weather data?**
A: Extend the feature engineering pipeline in `src/features/engineering.py` to include weather APIs like OpenWeatherMap.

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with ❤️ for a cleaner Delhi

[🔝 Back to top](#-delhi-air-quality-prediction--analysis)

</div>
