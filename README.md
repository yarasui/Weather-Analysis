# Household-Power-Prediction
forecasted power usage using regression and IoT data.
weatherHistory is a dataset retrieved from Kaggle via the following link: https://www.kaggle.com/datasets/muthuj7/weather-dataset/data
the dataset includes various weather features such as wind speed and humidity as well as the corresponding temperature.
# Outcome
random forest, gradient boosting, and xgboost all gave very high overall accuracy on the weather dataset, but their handling of the rare class (which is 'none' in my case) was different: random forest uses bagging, less prone to overfitting, but less powerful than boosting methods. its also easier to interpret. gradient boosting builds trees sequentially to correct residuals, but xgboost adds regularization, handles missing values by learning split directions, and is designed for speed/efficiency.

since real-world weather prediction often deals with imbalanced data and missing values,  xgboost is recommended as it is faster and more efficient than traditional boosting and also better at handling missing values, which is particularly useful in weather datasets

additional sources:https://www.geeksforgeeks.org/machine-learning/difference-between-random-forest-vs-xgboost/
