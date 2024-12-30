# Churn classification model.

# Project overview.
This project focused on analyzing customer churn rates for a bank with the ultimate goal of reducing churn. By examining the relationship between input features and churn rates, I aimed to provide actionable insights. The task was framed as a supervised classification problem, leveraging a labeled dataset to train a predictive model capable of identifying key factors influencing churn.

# Data cleaning and EDA analysis.
The dataset required minimal cleaning, as it was free of missing, inconsistent, or duplicate values, and all data types were appropriately formatted. Distribution analysis using histograms revealed that most features followed a normal distribution, with minimal outliers. For instance, the age column had a few values in the 80–90 range, which were retained as they provided valuable insights into older account holders. Given the dataset’s modest size, all available features were included in the analysis to maximize model performance.

# Machine learning & modelling.
1. Data preparation.
The dataset was split into input features (X) and the target variable (y), followed by training and testing splits. An initial imbalance was observed in the target variable, where the number of non-churning customers far exceeded those who churned. To address this imbalance, the SMOTE oversampling technique was employed, effectively balancing the classes.

2. Model selection and tuning.
A Random Forest Classifier was initially used for its robustness and interpretability. However, the model suffered from overfitting, performing exceptionally well on the training set but poorly on the test set.
To mitigate overfitting, CatBoost, a gradient boosting algorithm, was introduced. This approach significantly reduced variance and improved generalization. Cross-validation confirmed the model’s reliability, achieving an impressive average accuracy of 90%.

# Deployment.
To make the insights actionable, a Streamlit application was developed. This application allows users to input feature values and receive real-time churn predictions based on the CatBoost model. The solution offers both speed and accuracy, making it a valuable tool for decision-makers.
This workflow not only highlights the predictive power of machine learning but also ensures practical usability for business stakeholders aiming to reduce churn rates effectively.






