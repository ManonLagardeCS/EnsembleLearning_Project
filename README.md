# Exoplanet Detection Using Ensemble Learning

**Supervised by:** Myriam TAMI
**Authors:** Thomas Georges & Manon Lagarde

## Project Overview

Exoplanets—planets that orbit stars beyond our solar system—are crucial to understanding planetary formation and the potential for habitable worlds. The objective of this project is to develop a robust classification model using **ensemble learning techniques** to distinguish exoplanet candidates from false positives.

By utilizing ensemble learning models such as **Random Forest, Extra Trees, XGBoost, LightGBM, and AdaBoost**, we aim to enhance classification accuracy and determine the most effective approach for exoplanet detection.

## Dataset

The dataset consists of observations from **NASA's Kepler Mission**, which monitored over 150,000 stars for brightness variations caused by planetary transits.

- **Source:** [Kaggle - Kepler Exoplanet Search Results](https://www.kaggle.com/datasets/nasa/kepler-exoplanet-search-results)
- **Description:** Contains astrophysical measurements, including stellar flux, orbital period, and other key features for exoplanet classification.
- **Size:** ~9,000 records with multiple features per observation.
- **Data Type:** Numerical and categorical variables.

For a detailed breakdown of dataset columns, visit the [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html).

## Objectives & Methodology 

To classify stars as exoplanet candidates or non-candidates based on their observed properties, we will follow these steps :
### 1. Data Preprocessing

- **Feature Selection** : Removed non-necessary and administrative features
- **Handling Missing Values:** Used **mean imputation** for numerical features and removed features with excessive missing values.
- **Feature Engineering:** Created the binary target variable **`is_candidate`**, indicating whether an observation is an exoplanet candidate.
- **Correlation Analysis:** Removed low correlated features (<0.05) to the target and identified redundant features with correlation above 0.75.

These preprocessing steps help to improve classification accuracy.

### 2. Data Visualization

- Explore feature distributions and relationships.
- Analyze correlations between features and exoplanet classification.
- Use feature importance scores to guide model refinement.

### 3. Model Development

We will train and compare multiple ensemble learning models:

- **Random Forest**
- **Extremely Randomized Trees (Extra Trees)**
- **Gradient Boosting (XGBoost, LightGBM)**
- **AdaBoost**

### 4. Cross-Validation

- Implement **k-fold cross-validation** to evaluate model performance robustly.
- Ensure the model generalizes well by training on different subsets of data.
- Analyze validation results to select the optimal hyperparameter settings.
### **5. Model Evaluation**

- Assess performance using metrics such as:
    - Accuracy
    - Precision, Recall, and F1-score
    - ROC-AUC for assessing classification robustness
- Compare models and select the best-performing approach.
### **6. Hyperparameter Optimization**

- Fine-tune hyperparameters using techniques such as Grid Search and Randomized Search.
- Optimize models to improve predictive performance.

### **7. Report & Insights**

- Summarize preprocessing steps, model comparisons, and findings.
- Provide recommendations for further improvements and future research directions.

## Expected Outcomes

- Identification of the most effective ensemble model for exoplanet classification.
- A comparative analysis of ensemble methods, outlining strengths and limitations.
- A detailed report summarizing methodology, results, and recommendations for future studies.

## Acknowledgments

This project is part of a **Master of AI class project at CentraleSupélec**, supervised by **Myriam TAMI**.
