# Nordeus Data Science Challenge 2024 - Predicting User Activity

## Project Overview
This project focuses on predicting user activity in the first 28 days after users re-register to play Top Eleven, a popular mobile game. Using historical and recent re-registration data, we aim to forecast user engagement over this period. Accurate predictions will help Nordeus tailor personalized experiences and boost user retention for returning players.

## Problem Statement
User retention is a core challenge in mobile gaming. Re-engaging users who have uninstalled and later re-registered is an especially valuable opportunity. By analyzing their historical behavior and interactions upon re-registration, we can predict how active they’ll be in their first month back. This information enables the design of customized content and targeted re-engagement strategies, enhancing the gaming experience and increasing player retention.

The target variable in this project is the number of days a re-registered user is active during the first 28 days post re-registration, which is an integer between 0 and 28.

## Project Objectives
- Predict User Activity:
Develop a predictive model to forecast user activity for the first 28 days after re-registration.
Use multiple datasets covering both re-registration and historical gaming data.

- Enhance User Retention:
Deliver actionable insights for Nordeus to improve re-engagement and retention strategies based on predicted user activity levels.
Provide meaningful information for marketing and development teams to understand returning users’ needs.

## Data
The project includes four datasets:

- previous_lives_training_data.csv: Users' historical gaming behavior prior to re-registration.
- registration_data_training.csv: Data related to the day of re-registration.
- previous_lives_test_data.csv: Historical data of test users (without target variable).
- registration_data_test.csv: Re-registration data of test users (without target variable).

## Evaluation Metric
Model performance will be measured using Mean Absolute Error (MAE), which calculates the average absolute differences between the predicted and actual days active. Minimizing MAE will indicate higher accuracy in forecasting user activity levels.

## Expected Submission Format
The output file, days_active_first_28_days_after_registration_predictions.csv, should include:

- user_id: Unique identifier for each user in the test dataset.
- predicted_days_active_first_28_days_after_registration: Predicted integer value for days active during the first 28 days post re-registration.

### Example format:

![image](https://github.com/user-attachments/assets/c167c984-a3f4-4a5a-941c-c2fd183e02de)

## Technologies and Tools Used
- Programming Language: Python
- Libraries: Pandas, NumPy, Scikit-learn, LightGBM, XGBoost, TensorFlow, Optuna, SHAP
- Experiment Tracking: MLflow
- Visualization: Matplotlib, Seaborn, SHAP

## Results
- The best-performing model was the Feedforward Neural Network (FFNN), which achieved a Mean Absolute Error (MAE) of 5.45.
- Among traditional machine learning models, LightGBM performed the best, with an MAE of 5.95.
- The ensemble models (Stacking and Voting Regressors) provided a slight boost in performance but did not surpass the FFNN model.
- SHAP analysis indicated that features related to user engagement (e.g., playtime, days_active_lifetime and avg_stars_top_3_players) were the most influential in predicting user activity.

## Future Work
- Incorporate More Features: Include additional features from user activity logs or external sources (e.g., social media interactions) to improve prediction accuracy.
- Automated Retraining: Implement an MLOps pipeline for automated model retraining based on new data, ensuring the model remains accurate over time.
- Real-time Prediction Service: Deploy the model as an API service using FastAPI or Flask for real-time predictions and integration with Nordeus' production systems.
- Anomaly Detection: Add an anomaly detection module to identify unusual user behavior that may affect predictions.

## Key Takeaways
- The Feedforward Neural Network (FFNN) achieved the best performance, highlighting the importance of non-linear relationships in the data.
- LightGBM provided strong interpretability, making it a valuable model for understanding key drivers of user activity.
- The project demonstrated the effectiveness of hyperparameter tuning (Optuna) and feature selection in improving model accuracy.
- Future enhancements could focus on additional data sources and the implementation of real-time prediction capabilities.

