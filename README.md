# 🚑 Emergency Response Demand Analysis & Prediction

## 📓 Notebook

[View Full Analysis](notebooks/01_eda_modeling.ipynb)

## ⭐ Project Highlights
- Identified peak emergency demand windows using time-series analysis  
- Discovered distinct behavioral patterns across EMS, Traffic, and Fire incidents  
- Built a predictive model achieving ~91% accuracy for peak demand detection  
- Translated findings into actionable resource allocation strategies  

---

## 📌 Overview

This project analyzes 911 emergency call data to identify temporal demand patterns and build a predictive model for high-demand periods. The goal is to demonstrate how data-driven insights can support **resource allocation and operational planning** in emergency response systems.

---

## 🎯 Objectives

- Analyze call volume trends across time (hour, day, category)  
- Identify peak demand periods  
- Compare patterns across EMS, Traffic, and Fire incidents  
- Build a predictive model to identify high-demand periods  
- Translate findings into operational recommendations  

---

## 📊 Dataset

- **Source:** Kaggle – Montgomery County, PA 911 Calls  
- Includes:
  - Timestamp  
  - Call category (EMS, Traffic, Fire)  
  - Location data  

Time-based features were engineered from raw timestamps to support analysis and modeling.

---

## 🔍 Key Insights

### ⏱️ Temporal Patterns
- Call volume increases steadily from early morning and peaks in the late afternoon (~5 PM)  
- Lowest demand occurs overnight (11 PM – 4 AM)  

---

### 📅 Weekly Trends
- Weekday demand is consistently higher than weekends  
- Friday shows the highest overall call volume  
- Weekend demand decreases despite expectations of increased leisure-related incidents  

---

### 🚑 Category-Specific Patterns
- **EMS:** Peaks mid-morning (~10–11 AM), likely due to delayed symptom onset and healthcare system interactions  
- **Traffic:** Strong peaks during commuting hours (morning and late afternoon)  
- **Fire:** More evenly distributed, with increased activity during evening/night hours  

---

## 🤖 Predictive Modeling

### Approach
- Target: High-demand periods (top 25% of call volume)  
- Features:
  - Hour of day  
  - Day of week  
  - Weekend indicator  

---

### 📈 Results

| Model | Accuracy | Peak Recall | Peak Precision |
|------|--------|------------|---------------|
| Logistic Regression | 0.56 | 0.00 | 0.00 |
| Random Forest | 0.91 | 0.83 | 0.91 |

---

### 🧠 Interpretation

- Logistic Regression failed to capture peak demand patterns  
- Random Forest significantly outperformed, indicating:
  - Demand patterns are **nonlinear**
  - Time-based interactions are important  

These results demonstrate that even simple models can effectively identify high-demand periods when appropriate algorithms are used.

---

## 🚑 Operational Recommendations

- Increase staffing during:
  - Late afternoon peak hours  
  - Mid-morning EMS surge periods  
- Allocate traffic response resources during commuting windows  
- Maintain consistent EMS readiness due to steady demand  
- Use predictive models to anticipate high-demand periods  

---

## ⚠️ Limitations

- Model trained on aggregated time-based features only  
- Limited feature set (no weather, population density, or external factors)  
- Small test sample size — results should be validated on larger datasets  

---

## 🚀 Future Improvements

- Incorporate additional features (weather, holidays, geographic density)  
- Develop real-time prediction system  
- Build interactive dashboard (e.g., Streamlit)  
- Expand modeling to category-specific predictions  

---

## 🛠 Tools & Technologies

- Python  
- Pandas / NumPy  
- Seaborn / Matplotlib  
- Scikit-learn  
