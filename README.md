# 🏗️ Concrete Compressive Strength Predictor

*Machine learning models with uncertainty quantification and Streamlit deployment that predict concrete compressive strength for optimized construction mix design.*

![Construction](https://img.shields.io/badge/domain-construction_engineering-blue)
![Python](https://img.shields.io/badge/python-3.8%2B-green)
![ML](https://img.shields.io/badge/lightgbm-random_forest-orange)
![Deployment](https://img.shields.io/badge/deployed-streamlit-red)
![Accuracy](https://img.shields.io/badge/R²-0.914-green)

---

## 📋 Overview

I developed this project to solve the critical challenge of **optimizing concrete mix designs in construction projects**. Traditional methods rely on expensive trial mixes and extensive laboratory testing, which is time-consuming and increases project costs. I built an end-to-end machine learning solution that accurately predicts concrete compressive strength from mix proportions, complete with uncertainty quantification and a production-ready Streamlit web application for engineers and contractors.

**Industry Application:** Construction / Civil Engineering / Materials Engineering

---

## 🎯 The Problem

Construction projects face several concrete-related challenges:
- **Costly Trial Mixes:** Each test mix costs $500-$2000 in materials and lab testing
- **Time Delays:** 28-day curing time required for strength verification
- **Material Waste:** Suboptimal mix designs lead to over-engineering and waste
- **Safety Risks:** Under-designed mixes compromise structural integrity
- **Limited Expertise:** Small contractors lack access to mix design specialists

---

## 💡 The Solution

A comprehensive machine learning pipeline with web deployment:
1. **Advanced ML Models:** LightGBM and Random Forest regression with hyperparameter tuning
2. **Uncertainty Quantification:** Quantile regression for prediction intervals (5th, 50th, 95th percentiles)
3. **Production Deployment:** Interactive Streamlit web application for real-time predictions
4. **Feature Analysis:** Identified key drivers of concrete strength (Cement content most influential)

### Key Features:
- ✅ **High Accuracy:** Achieved R² = 0.914 on test data
- ✅ **Uncertainty Bounds:** Provides 90% prediction intervals for risk assessment
- ✅ **Production-Ready:** Complete Streamlit web application
- ✅ **Batch Processing:** Supports single predictions and CSV batch predictions
- ✅ **Interpretable Results:** Feature importance analysis and visualization

---

## 🛠️ Technical Implementation

### Technology Stack
- **Primary Language:** Python 3.8+
- **Core Libraries:** pandas, scikit-learn, LightGBM, matplotlib, seaborn
- **Deployment:** Streamlit, pickle for model serialization
- **Visualization:** Taylor diagrams, feature importance plots, uncertainty intervals

### Methodology
1. **Data Preparation:**
   - 1,030 concrete mix designs with compressive strength measurements
   - 8 input features: Cement, Blast Furnace Slag, Fly Ash, Water, Superplasticizer, Coarse Aggregate, Fine Aggregate, Age
   - Comprehensive exploratory data analysis and correlation analysis

2. **Model Development:**
   - **LightGBM:** Achieved best performance with R² = 0.914
   - **Random Forest:** Provided interpretable feature importance
   - **Hyperparameter Tuning:** GridSearchCV for optimal performance
   - **Cross-validation:** 80% train, 10% validation, 10% test split

3. **Uncertainty Analysis:**
   - Quantile regression for prediction intervals
   - 90% confidence bounds for engineering decisions
   - Comparative analysis using Taylor diagrams

4. **Web Application:**
   - Streamlit interface for easy access
   - Single prediction and batch CSV processing
   - Downloadable prediction results

---

## 📊 Results & Findings

### Model Performance Comparison

| Model | R² (Test) | RMSE (MPa) | MAE (MPa) | Key Strength |
|-------|-----------|------------|-----------|--------------|
| **LightGBM** | **0.914** | **4.65** | **3.19** | Best overall accuracy |
| **Random Forest** | 0.878 | 5.54 | 4.00 | Better feature interpretability |
| **Quantile Regression** | 0.90* | 4.8* | 3.3* | Provides uncertainty intervals |

*Average performance across quantiles

### Key Insights:
1. **Cement Content** was the most important predictor (49% correlation with strength)
2. **Water-Cement Ratio:** Critical factor affecting strength (negative correlation of -0.29)
3. **Age Impact:** Strength increases significantly with curing time (28 vs 365 days)
4. **Superplasticizer:** Positive impact on strength while reducing water requirement
5. **Fly Ash & Slag:** Supplementary materials that affect strength development
