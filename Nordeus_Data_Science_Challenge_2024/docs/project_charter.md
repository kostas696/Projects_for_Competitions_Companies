# Project Charter: Nordeus Data Science Challenge - Predicting User Activity

## 1. Project Title
Predicting User Activity for Nordeus - 2024 Job Fair Challenge

## 2. Project Background
Nordeus, a leader in mobile gaming, aims to deepen engagement and improve retention for its users. Specifically, returning players—those who uninstall and later re-register—offer a unique opportunity for re-engagement. By predicting the level of activity these users will display in the first 28 days post re-registration, Nordeus can craft tailored content and user experiences. This project aligns with Nordeus' commitment to providing personalized experiences and retaining its user base by identifying patterns in returning users’ behavior.

## 3. Business Objective
Goal: Increase user retention by tailoring experiences based on predicted activity levels of re-registered players.

Objectives:
- Improve Retention: Retaining re-registered users by predicting their future activity and offering tailored experiences based on their engagement patterns.
- Personalized User Experience: Enable targeted marketing and content development by identifying users likely to be highly engaged, allowing Nordeus to optimize their experience within the game.
By understanding returning players' behavior, Nordeus can enhance player satisfaction, extending their gaming life and increasing potential in-app engagement.

## 4. Technical Objective
Goal: Develop a robust and scalable machine learning pipeline to support ongoing model training, deployment, and monitoring within an MLOps framework.

Objectives:
- Data Processing Pipeline: Create a scalable pipeline to handle and preprocess incoming data from multiple sources, ensuring data quality and consistency.
- Feature Engineering and Storage: Develop engineered features to capture user behavior, and store these features in a manner that supports fast access and reuse.
- Model Training and Experiment Tracking: Implement a system for training and evaluating models using tracking tools like MLflow for comprehensive experiment tracking and model comparison.
- Deployment and Monitoring: Deploy the model in a production environment, using an API to serve predictions. Establish monitoring to track model performance, and detect issues such as data drift over time.
- Retraining Mechanism: Establish a manual retraining process based on performance monitoring rather than automated drift detection, ensuring the model remains relevant as user behaviors and app updates evolve.

## 5. Success Metrics
The project's success will be measured through a blend of accuracy, interpretability, and scalability metrics to ensure both business and technical goals are met.

Key Performance Indicators:
- Mean Absolute Error (MAE): Aim to achieve a low MAE for accurate predictions on the number of active days for returning users.
- Model Interpretability: Ensure the model is interpretable, allowing Nordeus' stakeholders to understand the primary drivers behind predicted activity levels.
- Scalability and Robustness:
Ensure the deployment is stable and can handle real-time inference for large user volumes.
Demonstrate adaptability of the pipeline to integrate new data sources and adapt to changes in user behavior.
- Pipeline Efficiency: Measure processing time from data ingestion to prediction, aiming for minimal latency to support potential real-time applications.
By achieving these success metrics, the project will support Nordeus in delivering a personalized gaming experience and improving user retention through data-driven insights.