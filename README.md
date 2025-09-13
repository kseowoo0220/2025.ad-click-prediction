# Ad Click Prediction

This project predicts whether a user will click on an online advertisement (ad) based on demographic and contextual features.  
The workflow includes **EDA, feature engineering, multicollinearity checks, model building (Logistic Regression vs XGBoost), performance evaluation, and business insights**.  

---

## Dataset
- **Sample size**: 814 users  
- **Target variable**: `click` (1 = clicked, 0 = not clicked)  
- **Original features**: 9 variables  

### Features
- **id**: Unique identifier for each user  
- **full_name**: User's name formatted as `"UserX"` for anonymity  
- **age**: Age of the user (18–64 years)  
- **gender**: Gender (Male, Female, Non-Binary)  
- **device_type**: Device used to view the ad (Mobile, Desktop, Tablet)  
- **ad_position**: Ad position on the webpage (Top, Side, Bottom)  
- **browsing_history**: User’s browsing activity before seeing the ad (Shopping, News, Entertainment, Education, Social Media)  
- **time_of_day**: When the user viewed the ad (Morning, Afternoon, Evening, Night)  
- **click**: Target label (1 = clicked, 0 = not clicked)  

---

## Workflow
1. **Exploratory Data Analysis (EDA)**  
   - Distribution of `click` variable  
   - CTR differences by age group, gender, device, ad position, browsing history, time of day  

2. **Feature Engineering**  
   - Created categorical variable `age_group`  
   - One-hot encoding for categorical predictors  

3. **Multicollinearity Check**  
   - Correlation heatmap  
   - Variance Inflation Factor (VIF) → no significant multicollinearity  

4. **Modeling**  
   - **Logistic Regression** as baseline model  
   - **XGBoost** as main predictive model  
   - ROC-AUC comparison and ROC Curve visualization  

---

## Final Results & Business Insights

### Model Performance
- **Logistic Regression (Baseline)**  
  - ROC-AUC: **0.523**  
  - Provides interpretability but limited predictive power.  

- **XGBoost (Main Model)**  
  - ROC-AUC: **0.826**  
  - Delivers substantially stronger predictive performance and captures complex feature interactions.  

➡️ **XGBoost was selected as the final model** due to its superior accuracy and robustness.  

---

### Key Predictors
- **Age group (30s)** – Strongest predictor of ad clicks  
- **Time of Day (Night)** – Higher engagement at night  
- **Ad Position (Top, Side)** – Placement strongly impacts CTR  
- **Browsing History (News)** – News readers more likely to click ads  
- **Device Type (Mobile, Tablet)** – Supports mobile-first strategy  

---

### Strategic Takeaways
1. **Targeting**: Focus on **younger demographics (30s)**  
2. **Timing**: Run campaigns in **evening/night hours**  
3. **Placement**: Prioritize **top/side ad positions**  
4. **Personalization**: Use browsing history for **context-relevant ads**  

---

## Tech Stack
- **Python**: Pandas, NumPy, Scikit-learn, Statsmodels, XGBoost  
- **Visualization**: Matplotlib, Seaborn  
- **Notebook**: Jupyter  


