# 🦠 H1N1 Vaccination Prediction Project

---

## 📌 1. Project Overview
This project predicts whether individuals received the H1N1 flu vaccine using data from the **National 2009 H1N1 Flu Survey**.

The goal is to build a **binary classification model** that estimates the probability of vaccination based on:
- Demographics  
- Health behaviors  
- Public perceptions  

---

## 🎯 2. Business Understanding

Vaccination is an important public health tool, but many people do not get vaccinated due to **hesitancy, misinformation, and access issues**.

- **Problem:** Identify people who are likely or unlikely to get vaccinated  
- **Stakeholders:** Public health organizations, policymakers, healthcare providers  
- **Key Question:** What factors most influence vaccine uptake?

---

## 📊 3. Data Description

- **Number of Records:** 26,707  
- **Number of Features:** 38  

**Target Variable:**  
- `h1n1_vaccine`  
  - 0 = Not Vaccinated  
  - 1 = Vaccinated  

**Feature Categories:**
- **Behavioral:** Mask use, hand washing, social distancing  
- **Perceptions:** Vaccine effectiveness, perceived risk  
- **Demographics:** Age, education, race, income  

**Challenges:**
- Missing values in some features (e.g., health insurance, employment)
- Handled using imputation

---

## 🔍 4. Exploratory Data Analysis (EDA)

EDA was performed to understand patterns in the data and relationships with vaccination.

### 📈 Example Visualization
![EDA Example](images/eda_plot.png)

Key observations:
- People who believe the vaccine is effective are more likely to take it  
- Higher perceived risk increases vaccination likelihood  
- Doctor recommendation strongly influences decisions  

---

## ⚙️ 5. Methodology

1. **Data Cleaning**
   - Handled missing values
   - Encoded categorical variables  

2. **Handling Imbalance**
   - Applied **SMOTE** to balance classes  

3. **Modeling**
   - Logistic Regression  
   - Decision Tree  

4. **Hyperparameter Tuning**
   - Used **GridSearchCV** to improve performance  

---

## 📊 6. Model Performance

| Model | AUC Score |
|------|----------|
| Decision Tree (Base) | 0.649 |
| Decision Tree (Tuned) | 0.804 |
| Logistic Regression (Tuned) | **0.821** |

### 📉 Model Comparison
![Model Performance](images/model_performance.png)

👉 Logistic Regression performed best overall.

---

## ⭐ 7. Key Insights (Top Predictors)

The most important factors influencing vaccine uptake:

- Doctor recommendation (strongest predictor)
- Belief in vaccine effectiveness
- Being a health worker
- Age (older individuals more likely)
- Perceived risk of H1N1  

### 📊 Feature Importance Visualization
![Feature Importance](images/feature_importance.png)

---

## ✅ 8. Conclusions

- Model performance improved significantly after tuning  
- Logistic Regression achieved the highest AUC (0.821)  
- Behavioral and perception-based features are strong predictors  

---

## 💡 9. Recommendations

1. Focus on **doctor recommendations** to increase vaccination rates  
2. Target people with **low perceived risk or low trust** in vaccines  
3. Use model predictions to guide **public health campaigns**  
4. Continuously update the model with new data  
5. Improve data quality for better predictions  

---

## ▶️ 10. How to Run the Project

### Requirements:
- Python 3.x  
- Jupyter Notebook  

### Libraries:
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- imblearn  

### Steps:
1. Open `index.ipynb`  
2. Run all cells  
3. Reproduce results and visualizations  

---

## 📁 Project Structure
