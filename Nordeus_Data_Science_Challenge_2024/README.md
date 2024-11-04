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

user_id,predicted_days_active_first_28_days_after_registration
12345,15
67890,8
...
