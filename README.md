# StudentPerformance-ML
Predicting student mathematics performance using machine learning models and identifying key academic predictors.

### Overview

This project investigates whether machine learning models can accurately predict **student Mathematics scores** using prior academic performance and school-related metadata, and which subjects influence math outcomes the most.

I worked with a dataset of **16,824 student records** from schools in **Halabja** across five academic years (2018–2023), containing grades in multiple subjects and basic academic metadata.

The project compares **Linear Regression** and **Random Forest Regression**, and uses **feature importance analysis** to understand which subjects are most strongly linked to Mathematics performance.

---
###  Dataset

- **Source:** Public student grade dataset from schools in Halabja (2018–2023)  
- **Size:** 16,824 records  
- **Attributes (20 total):**
  - **Metadata:** Serial number, School Name, Class, Academic Year  
  - **Subjects:** Kurdish, Arabic, English, Mathematics, Physics, Chemistry, Biology, Computer, History, Geography, Economics, Sociology, Philosophy, Science

The **target variable** is the **Mathematics grade**.  
All other subject grades and metadata are used as input features.

**Preprocessing steps:**

1. **Categorical encoding:**  
   - School Name, Class, and Academic Year were encoded using one-hot encoding.
2. **Missing values:**  
   - Missing numeric values were imputed using the mean of each column.
3. **Train-test split:**  
   - 80% of the data for training, 20% for testing.

---

###  Models Used

I implemented and compared:

- **Linear Regression**
  - Baseline model assuming a linear relationship between features and math scores.
- **Random Forest Regression**
  - Ensemble of decision trees that can capture nonlinear relationships and interactions between subjects.

---

### 📏 Evaluation Metrics

Models were evaluated with:

- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

These metrics measure how far predictions are from actual Mathematics scores (in points).

---

### ✅ Main Results

From the experiments:

| Model            | MAE   | RMSE  |
|------------------|-------|-------|
| Linear Regression| 7.49  | 9.54  |
| Random Forest    | 7.21  | 9.28  |

- **Random Forest achieved lower prediction error** (both MAE and RMSE) than Linear Regression.
- This confirms that **nonlinear methods** like Random Forest can better capture the relationships between school subjects and Mathematics performance.

---

### 🔍 Feature Importance (Random Forest)
Random Forest feature importance analysis showed that:

- **English**
- **Science**
- **Kurdish**

were among the **most influential subjects** for predicting Mathematics scores.

This suggests that:

- language and reading-related skills (e.g., English)  
- and scientific reasoning (Science)  

may support better performance in Mathematics, for example through improved problem understanding and logical thinking.

---

### 🧠 What I Learned

This project helped me practice:

- working with a **real-world educational dataset**  
- handling **missing values** and **categorical encoding**  
- training and comparing **regression models**  
- evaluating models with **MAE and RMSE**  
- using **feature importance** to interpret Random Forest models  
- thinking critically about how data is used in **educational decision-making**

It also showed me how **effort, context, and subject interdependencies** all play a role in student performance, not just “raw ability”.

---

### 🧪 Code & Reproducibility

The main experiment notebook is available here:

- `notebooks/student_math_scores_ml.ipynb`

It includes:

- data loading and preprocessing  
- training Linear Regression and Random Forest models  
- computing MAE and RMSE  
- extracting and saving feature importances

---

###  Research Paper

The full write-up of this project, including references and figures, is available here:

(https://docs.google.com/document/d/174mjH76ykIQsgckZnke4YqxIH_0GhmXn/edit?usp=sharing&ouid=109869815623350786125&rtpof=true&sd=true)

This document follows a formal structure (Abstract, Introduction, Methodology, Results, Conclusion) and cites related work on student performance prediction using machine learning.

---

###  Future Work

Possible extensions include:

- trying additional models (e.g., Gradient Boosting, XGBoost)  
- adding socio-economic or behavioral variables  
- testing generalization across other regions or school systems  
- exploring fairness and bias to ensure that predictions do not disadvantage specific student groups

---

*Author: **Mayssae El Bazi***  
