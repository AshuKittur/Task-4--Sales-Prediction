# Task-4--Sales-Prediction
This repository contains a project focused on building a sales prediction model using machine learning. The goal is to forecast product sales based on various features and provide actionable insights that businesses can use to optimize their marketing strategies.

Objectives

Data Preprocessing:

Clean the dataset by handling missing values and removing outliers to ensure the model receives high-quality data. Missing values in critical columns were removed, and Z-scores were used to identify and eliminate outliers.

Normalize numerical features to bring all data into a comparable scale.

Exploratory Data Analysis (EDA):

Visualize the dataset to understand relationships between variables and detect issues like multicollinearity or skewness.

Use scatter plots and correlation heatmaps to gain insights into the data.

Feature Engineering:

Create new features such as salary_to_debt_ratio, debt_to_net_worth_ratio, and log_net_worth to capture meaningful relationships in the data.

Model Building and Tuning:

Implemented the LightGBM regressor for sales prediction due to its efficiency and accuracy for tabular data.

Optimized the model using GridSearchCV to fine-tune parameters like max_depth, n_estimators, and learning_rate.

Model Evaluation:

Evaluate the model using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²) to assess its performance.

Compare results before and after optimization to highlight improvements.

Dataset

The dataset consists of sales-related data, including numerical and categorical features like salary, debt, net worth, and country of residence. Key steps in data processing included:

Dropping unnecessary columns such as customer names and emails.

Imputing missing values in numerical columns with the median.

Removing outliers using Z-scores to ensure consistent model performance.

Encoding categorical variables and normalizing numerical features.

Key Challenges

Handling Missing Data:

Missing values in critical columns were removed to maintain data integrity. For numerical columns, the median was used to impute missing values.

Outliers:

Used Z-score analysis to remove rows with extreme values (Z > 3). This ensured that the model wasn’t affected by skewed data.

Feature Engineering:

Adding features like salary_to_debt_ratio and log_net_worth required careful thought to avoid introducing multicollinearity or unnecessary complexity.

Hyperparameter Tuning:

Fine-tuning the LightGBM model with GridSearchCV was time-intensive, but it significantly improved the accuracy and robustness of predictions.

Results

Initial Model Performance:

MAE: ~1365

MSE: ~3.4 million

R²: ~0.96

Final Model Performance (after optimization):

MAE: 1190.39

MSE: 2.46 million

R²: 0.9768

The improvements in metrics highlight the effectiveness of hyperparameter tuning and feature engineering.

Usage

Upload the dataset to your working directory.

Follow the steps in the notebook to preprocess the data, build the model, and evaluate its performance.

Conclusion

This project demonstrates how thoughtful data preprocessing, feature engineering, and model optimization can lead to accurate sales predictions. The final model provides actionable insights for businesses to understand sales trends and optimize their marketing strategies effectively.
