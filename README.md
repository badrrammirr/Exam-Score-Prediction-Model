# Machine Learning Project: Student Exam Score Prediction

## Project Overview

This project focuses on building a supervised machine learning regression model to accurately predict a student's final exam score. The model leverages behavioral and demographic features to quantify the influence of factors like study habits, class attendance, and available resources on academic performance. The primary objective is to provide actionable, data-backed insights for targeted educational strategies.

## Key Results and Model Performance

The project utilizes a **Random Forest Regressor**, selected for its ability to effectively handle non-linear data relationships and provide feature importance metrics.

| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Model ($R^2$ Score)** | **~[Insert Your R^2 Score Here]** | The model explains approximately **[Your R^2 score in percentage]%** of the variance observed in the exam scores. |
| **Prediction Error (MAE)** | **~[Insert Your MAE Score Here]** | On average, the model's prediction deviates by $\pm$ **[Your MAE Score]** points from the true score. |

---

## Analytical Findings: Feature Importance

Feature Importance analysis was performed to isolate the factors with the highest predictive power.

The analysis clearly identified [ Study Hours and Class Attendance] as the strongest drivers of exam scores. Specifically, [ 'Study Hours' contributed over 40% of the model's predictive power].

---

## Technical Implementation

### Core Tools
* **Language:** Python
* **Libraries:** `Pandas`, `NumPy`, `Scikit-learn`, `Matplotlib`, `Seaborn`
* **Dataset:** `Exam_Score_Prediction.csv`

### ML Workflow and Pipeline Structure
The entire process is encapsulated in a reliable **Scikit-learn `Pipeline`**:

1.  **Preprocessing:** A **`ColumnTransformer`** was used for concurrent handling of diverse feature types:
    * Numerical features were scaled using `StandardScaler`.
    * Categorical features were converted using `OneHotEncoder`.
2.  **Training:** The clean, transformed data was fed into the **`RandomForestRegressor`** (`'regressor'` step in the pipeline) for training.
3.  **Evaluation:** The model's performance was confirmed through multiple metrics and visual checks (Residual Plots, Actual vs. Predicted).

### Visualizations
The project notebook includes essential plots that visually validate the model and showcase the data:
* Actual vs. Predicted Scores Scatter Plot
* Residual Plot for error analysis
