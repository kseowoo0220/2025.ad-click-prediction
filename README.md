# Ad Click Prediction

## Project Overview
This project focuses on **predicting whether a user will click on an online advertisement** using demographic and contextual features.  
The main objective is to **improve ad targeting and campaign efficiency** by identifying the most influential factors driving ad clicks.

---
## Dataset
- **Size**: 814 observations, multiple categorical & numerical features
- **Key Features**:
  - Age group
  - Gender
  - Device type (Mobile, Tablet, Desktop)
  - Time of day (Morning, Afternoon, Night)
  - Ad position (Top, Side, Bottom)
  - Browsing history category
- **Target Variable**: `click` (1 = clicked, 0 = not clicked)

---
## Data Preprocessing
- **Missing Values**: no missing and outlier in dataset
- **Encoding**: One-hot encoding for categorical features
- **Feature Scaling**: Standardized numerical features
- **Train-Test Split**: 80/20 ratio

---
## Exploratory Data Analysis
Key findings from EDA:
- Younger users (20s, 30s) show higher click-through rates (CTR)
- Mobile and tablet users engage more compared to desktop
- Ads placed at the top or side are more effective
- Nighttime shows significantly higher CTR

Visualizations:
- CTR by each group

---
## Modeling
Two models were implemented:

1. **Logistic Regression (Baseline)**
   - ROC-AUC: 0.523
   - Strength: Interpretability
   - Limitation: Weak predictive power

2. **XGBoost (Final Model)**
   - ROC-AUC: 0.826
   - Strength: Captures non-linear relationships and feature interactions
   - Selected as the final model due to superior performance

---
## Feature Importance (XGBoost)
Top predictors of ad clicks:
1. Age group (30s)
2. Time of day (Night)
3. Ad position (Top, Side)
4. Browsing history (News)
5. Device type (Mobile, Tablet)

---
## Business Insights
- **Target younger demographics (30s)** for higher engagement
- **Nighttime campaigns** yield stronger click-through performance
- **Prioritize premium ad positions** (Top, Side) for visibility
- **Mobile-first strategy** is validated
- **News content alignment** enhances ad relevance

