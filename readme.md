# Student Depression Classifier

## Project Overview
**Aim:** To develop and optimize machine learning models to predict depression likelihood in students. This project focuses on tuning hyperparameters and comparing accuracy using F1-scores and cross-validation to identify the most robust predictive model.

## Data Source
**Source:** [Student Depression Dataset (Kaggle)](https://www.kaggle.com/datasets/hopesb/student-depression-dataset)

**Dataset Statistics:**
* **Observations:** 27,899
* **Total Features:** 18

**Key Features Analyzed:**
`Academic.Pressure` | `Work.Pressure` | `Job.Satisfaction` | `Sleep.Duration` | `Financial.Stress` | `Work.Study.Hours` | `Dietary.Habits`

## Methodology & Key Steps
The analysis followed a rigorous data science pipeline:

* **Exploratory Data Analysis (EDA):** Analyzed distributions and class balances.
* **Data Cleaning:** Identified and handled missing data; treated outliers.
* **Feature Engineering:** Performed feature encoding and selection based on correlation matrices.
* **Normalization:** Applied feature normalization to ensure model stability.
* **Model Tuning:** Conducted hyperparameter tuning and Cross-Validation.

## Classifiers Built & Results
Several models were trained to benchmark performance.

| Model | Training Accuracy | Test Accuracy |
| :--- | :--- | :--- |
| **Logistic Regression** | 86.4% | 86.3% |
| **Random Forest** | 84.7% | 86.3% |
| **Ensemble Model** (RF + LogReg) | -- | 86.0% |
| **Support Vector Machine (SVM)** | 86.6% | 73.5% |
| **Neural Network** | *Did not converge* | -- |

## Conclusion & Insights
1.  **Best Performer:** The **Logistic Regression** model achieved the highest consistent accuracy (86.3%). This suggests the underlying data boundaries are largely linear.
2.  **Random Forest:** Capped at the highest accuracy with **200 trees**, confirming that increasing complexity beyond this point yielded diminishing returns.
3.  **Overfitting:** The SVM model showed signs of overfitting (High Training score vs. Low Test score).
4.  **Neural Network:** The model did not converge within the computational time constraints, suggesting that simpler models (like Logistic Regression) are more efficient for this specific dataset structure.

---
*Project by Aditya Daware*
