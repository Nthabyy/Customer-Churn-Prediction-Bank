# Customer Churn Prediction Model

## Problem Statement

Customer churn prediction is crucial for businesses to retain valuable customers and improve customer satisfaction. The goal of this project is to build a machine learning model that can predict whether a customer is likely to churn (leave the service) based on various features such as customer demographics, usage patterns, and other service-related factors.

### Key Steps in the Process:
- **Data Cleaning**: Identifying and handling missing or inconsistent data.
- **Exploratory Data Analysis (EDA)**: Understanding the data's underlying patterns and distributions.
- **Data Preprocessing**: Transforming and scaling the data for better model performance.
- **Model Building**: Using algorithms to predict churn probability.
- **Model Explainability**: Using SHAP and LIME to interpret the model's predictions.

## Data Preparation

### 1. **Cleaning the Data**
The first step in the data preparation process is cleaning. This involves:
- **Checking for duplicates**: Ensuring that there are no repeated entries in the dataset.
- **Handling inconsistent data**: Identifying and resolving any discrepancies or erroneous entries in the data.

### 2. **Exploratory Data Analysis (EDA)**
The goal of EDA is to understand the data and uncover hidden patterns. Various techniques are used to visualize the data and check the distribution of features:
- **Seaborn** and **Matplotlib** are used for visualizing distributions, correlations, and other statistical relationships.
- **Plotly** is used for interactive plots that help in a more intuitive understanding of complex relationships.

### 3. **Data Preprocessing**
Preprocessing is critical to transforming the raw data into a format suitable for machine learning models:
- **Handling Outliers**: We used techniques such as percentile-based filtering to remove extreme values that may affect model performance.
- **Standardization**: We applied standard scaling to ensure that all features are on the same scale, which is crucial for algorithms like Logistic Regression or KNN.
- **One-Hot Encoding**: Categorical variables are converted into numeric representations using one-hot encoding, which transforms each category into a binary column.

### 4. **Data Transformation**
- **Standardization**: We applied standardization to the dataset to scale the features to have a mean of 0 and a standard deviation of 1, improving the model's ability to converge faster.

## Model Algorithms

We used the **Random Forest Classifier** for predicting customer churn. Random Forest is an ensemble learning method that combines multiple decision trees to improve the model’s accuracy and robustness.

## Model Explainability

To understand how the model makes predictions, we used the following model explanation methods:
- **SHAP (SHapley Additive exPlanations)**: SHAP provides a unified measure of feature importance and allows us to understand the contribution of each feature to the final prediction.
- **LIME (Local Interpretable Model-agnostic Explanations)**: LIME explains the model's predictions by approximating the model with an interpretable one, showing the contribution of each feature to the decision.

## Model Evaluation Results

### Power BI Analysis

![Power BI Analysis](https://github.com/Nthabyy/Customer-Churn-Prediction-Bank/blob/master/BI%20Analysis%20Customer%20Churn.png?raw=true)

### Model Evaluation Heatmap

![Model Evaluation Heatmap](https://github.com/Nthabyy/Customer-Churn-Prediction-Bank/blob/master/Picturues/Model-eva-%20Heatmap.png?raw=true)

### Model Analysis using Lime

![Model Analysis Lime](https://github.com/Nthabyy/Customer-Churn-Prediction-Bank/blob/master/Picturues/Model-Analysis%20Lime.png?raw=true)

## Model Evaluation

## Model Evaluation Results

We evaluated the model's performance using the following metrics:

| Class  | Precision | Recall | F1-Score | Support |
|--------|-----------|--------|----------|---------|
| 0      | 0.86      | 0.96   | 0.91     | 1607    |
| 1      | 0.71      | 0.36   | 0.48     | 393     |

**Accuracy**: 0.85 (2000 samples)

| Metric       | Value |
|--------------|-------|
| Macro avg    | 0.79  | 
| Weighted avg | 0.83  |


## Conclusion

In this project, we successfully built a customer churn prediction model using **Random Forest**. The model achieved an accuracy of 85% on the test dataset. We also used advanced techniques like **SHAP** and **LIME** for model explainability to understand the feature importance and decision-making process of the model. The model can help businesses identify customers at risk of churning, allowing them to take preventive measures to retain valuable customers.
