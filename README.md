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
