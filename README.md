# Salary Range Prediction Using Machine Learning

## Project Overview
This project develops a **Machine Learning classification system** that predicts **salary ranges (Low, Medium, High)** for employees in tech organizations.  
Instead of predicting exact salary figures, the system focuses on salary ranges to better align with real-world Human Resource (HR) compensation practices.

---

## Problem Statement
Salary decisions in many technology organizations often rely on subjective judgment, past experiences, or informal standards. This can lead to:

- Inconsistencies in salary allocation  
- Potential bias and unfairness  
- Employee dissatisfaction  
- Difficulty scaling compensation decisions as organizations grow  

Manual decision-making becomes increasingly unreliable in large and diverse organizations.

---

## Solution Approach
A **Supervised Machine Learning Classification Model** was developed to predict salary ranges rather than exact amounts.

Multiple algorithms were evaluated, including:

- Logistic Regression  
- Random Forest  
- Support Vector Machine (SVM)  
- Decision Tree  
- K-Nearest Neighbors (KNN)  
- Gradient Boosting  

**Gradient Boosting** achieved the best overall performance and was selected as the final model.

The system enables HR teams to:

- Standardize salary recommendations  
- Improve fairness and transparency  
- Support data-driven compensation decisions  
- Reduce subjective bias in salary allocation  

---

## Dataset Description
- **Dataset Size:** 10,000 rows × 18 columns  
- **Data Types:**  
  - Numerical: 8  
  - Categorical: 10  

### Key Features
- Age  
- Gender  
- Education Level  
- Years of Experience  
- Job Role  
- Skill Score  
- Certifications  
- Performance Score  
- Projects Completed  
- Employment Type  
- Company Size  
- Location  
- Monthly Salary (Target converted to Salary Range)

---

## Data Quality Observations
- 423 missing values in `years_experience`  
- Outliers observed above 20 years of experience  
- Inconsistent categorical labels in `education_level`  
- Other columns were complete and well distributed  

Overall, the dataset was suitable for modeling after preprocessing.

---

## Data Cleaning & Preprocessing
The dataset was cleaned using the following steps:

- Imputed numerical missing values using **median**
- Filled categorical missing values using **mode**
- Standardized text fields (lowercase, removed spaces)
- Replaced abbreviations:  
  - `BSc → bachelor`  
  - `MSc → master`  
  - `Ph.D → phd`
- Capped outliers in `years_experience` at **16 years**
- Applied **One-Hot Encoding** for categorical variables
- Used **Scaling (StandardScaler / MinMaxScaler)** for numerical features

---

## Exploratory Data Analysis (EDA) – Key Insights

### 1. Distribution of Salary Ranges
- Dataset heavily skewed toward **High Salary**
- Medium salary moderately represented
- Low salary least common
- Suggests a high-earning organizational environment

### 2. Salary Range vs Education Level
- High salaries dominate across all education levels
- Bachelor’s holders form the largest high-income group
- Master’s and PhD distributions are similar
- Even High School graduates show strong high-income presence, indicating a niche dataset

---

## Tools & Libraries
### Numerical & Data Handling
- NumPy  
- Pandas  

### Visualization
- Matplotlib  
- Seaborn  

### Machine Learning
- Scikit-learn  

Key Modules Used:
- ColumnTransformer  
- Train/Test Split  
- StandardScaler & MinMaxScaler  
- OneHotEncoder  
- Pipeline  
- Multiple Classifiers  
- Evaluation Metrics (Accuracy, F1, ROC-AUC, Precision, Recall)

---

## Model Evaluation Metrics
Models were evaluated using:

- Accuracy Score  
- F1 Score  
- Precision  
- Recall  
- ROC-AUC Score  
- Confusion Matrix  
- ROC Curve  

**Gradient Boosting produced the most balanced and reliable performance.**

---

## How to Run the Project
- Clone the repository
- Install dependencies from requirements.txt
- Open the Jupyter Notebook
- Run all cells

---

## Project Structure
salary-range-prediction-ml/
│
├── data/
├── notebooks/
├── images/
├── src/
├── README.md
└── requirements.txt

---

## Conclusion
This project demonstrates how Machine Learning can support **fair, transparent, and scalable salary decision-making** in tech organizations.  
By predicting salary ranges rather than exact figures, the model aligns better with real HR policies and reduces subjective bias while improving consistency.

---

## Author
**Twizihirwe Benjamin**  
Machine Learning & Data Enthusiast  

- LinkedIn: https://linkedin.com/in/benjamin-twizihirwe-6a6830358
- GitHub: https://github.com/Benjamin005


