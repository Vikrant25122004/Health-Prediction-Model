# Health and Lifestyle Data Analysis and Predictive Modeling

## Project Overview

This project explores a dataset containing health and lifestyle metrics to analyze patterns, understand relationships between various factors and medical conditions, and build predictive models for medical condition classification and hospital length of stay. The analysis involves data cleaning, exploratory data analysis through correlations and visualizations, and machine learning model development and evaluation.

## Dataset

The dataset, `dirty_v3_path.csv`, contains health and lifestyle metrics for a collection of patients. Key columns include:

*   **Target Variable:** `Medical Condition` (e.g., 'Diabetes', 'Healthy', 'Hypertension', 'Cancer', 'Obesity', 'Asthma', 'Arthritis')
*   **Health Metrics:** `Glucose`, `Blood Pressure`, `BMI`, `Cholesterol`, `HbA1c`, `Oxygen Saturation`
*   **Lifestyle/History:** `Smoking`, `Alcohol`, `Physical Activity`, `Diet Score`, `Family History`, `Stress Level`, `Sleep Hours`
*   **Demographics:** `Age`, `Gender`
*   **Other:** `LengthOfStay`, `random_notes`, `noise_col`

The dataset was identified as "dirty," requiring preprocessing to handle missing values and inconsistent data.

## Methodology

The project followed a standard data science methodology:

1.  **Data Loading and Initial Inspection:** Loading the dataset and assessing its structure and quality.
2.  **Data Cleaning and Preprocessing:** Handling missing values (dropping rows for missing Gender, imputing others with mean or mode) and removing irrelevant features (`random_notes`, `noise_col`). Categorical features were encoded using Label Encoding.
3.  **Exploratory Data Analysis (EDA):** Analyzing correlations between key variables (Age, Physical Activity, Sleep Hours, Stress Level, Cholesterol) and visualizing distributions and relationships through scatter plots and histograms. Investigating the demographic and lifestyle characteristics of patients with specific medical conditions.
4.  **Predictive Modeling:**
    *   **Medical Condition Classification:** A Random Forest Classifier was trained to predict the medical condition based on health and lifestyle features.
    *   **Hospital Length of Stay Prediction:** A Random Forest Regressor was trained to predict the length of hospital stay.
5.  **Model Evaluation:** Assessing the performance of the classification model using accuracy, precision, recall, and F1-score, and the regression model using MAE, MSE, RMSE, and R2 score.

## Key Findings and Insights

*   **Correlations:** Weak to moderate linear relationships were observed between various health and lifestyle factors. Notable correlations included a moderate negative association between Physical Activity and BMI, and a moderate positive association between Physical Activity and Diet Score. Age, Sleep Hours, and Stress Level showed weaker correlations with most health metrics.
*   **Medical Condition Profiles:** Analysis of individual medical conditions revealed varying age and gender distributions. Lifestyle factors like smoking and alcohol consumption were also analyzed within these groups, highlighting their presence in patients with conditions like Diabetes.
*   **Medical Condition Classification:** The Random Forest Classifier achieved an accuracy of around 78.6%. While promising, evaluation metrics suggested challenges in accurately classifying all conditions, potentially due to class imbalance.
*   **Hospital Length of Stay Prediction:** The Random Forest Regressor for Length of Stay prediction had an R2 score of 0.29, indicating that the current features explain a limited portion of the variability in hospital stay duration. The MAE of 1.57 suggests an average prediction error of about 1.57 days.

## Code Structure

The notebook is organized into sections covering:

*   Data Analysis and Features
*   Data Preprocessing and Feature Engineering
*   Medical Condition Classification (Code and Analysis)
*   Hospital Length of Stay Prediction (Code and Analysis)
*   Correlation Analyses (Age, Physical Activity, Sleep Hours, Stress Level, Cholesterol - Code and Analysis)
*   Medical Condition Specific Analyses (Hypertension, Asthma, Obesity, Cancer, Healthy, Arthritis, Diabetes - Code and Analysis)
*   Conclusion

Each code block is accompanied by a markdown explanation of its purpose and the statistical insights gained.

## Future Work

Potential future steps to enhance this project include:

*   Further feature engineering to create more informative variables.
*   Exploring advanced machine learning algorithms for both classification and regression tasks.
*   Implementing techniques to address class imbalance in the medical condition classification.
*   Incorporating additional relevant data sources to improve prediction accuracy, especially for Length of Stay.
*   Hyperparameter tuning to optimize model performance.

This README provides a summary of the project's journey in analyzing health and lifestyle data and building predictive models, highlighting key findings and areas for future exploration.
