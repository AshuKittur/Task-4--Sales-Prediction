# Sales Prediction Tool

This project focuses on predicting product sales using various factors like advertising spend, target audience segmentation, and platform selection. The main goal was to create a machine learning model that businesses can use to understand future trends and optimize marketing strategies. Below, I’ve detailed what I did, the challenges I faced, and how I tackled them.

## Objectives

1. **Data Preprocessing:**

Ensure the dataset is clean and ready for analysis. This included handling outliers, scaling numerical features, and encoding categorical data to make it suitable for machine learning models.

2. **Understand the Data:**  
   Before jumping into modeling, I explored the data with scatter plots and heatmaps to find correlations and trends. This was key to deciding which features to focus on.

3. **Enhance the Dataset:**  
   I created new features like `salary_to_debt_ratio` and `debt_to_net_worth_ratio` to provide better insights. I also normalized numeric features so the model could train effectively.

4. **Train a Predictive Model:**  
   I used LightGBM for the task, as it’s fast and handles large datasets well. GridSearchCV helped tune hyperparameters, and metrics like RMSE and R² were used to evaluate the model.

## Approach

1. **Data Preprocessing**  
   - Cleaned missing values and dropped irrelevant columns (e.g., customer name and email).  
   - Removed outliers using Z-score filtering with a threshold of 3.  
   - Normalized the numeric data to improve model performance.

2. **EDA (Exploratory Data Analysis)**  
   - Plotted a scatterplot of annual salary vs. car purchase amount, colored by gender, to understand trends.  
   - Generated a heatmap to check for correlations.

3. **Feature Engineering**  
   - Added ratios and logarithmic transformations to make features more meaningful. These additional features helped capture relationships not immediately obvious from the raw data.

4. **Model Selection and Training**  
   - Chose LightGBM due to its speed and efficiency for regression problems.  
   - Used GridSearchCV for hyperparameter tuning, testing combinations of depth, leaves, and learning rates.

5. **Evaluation**  
   - The initial MAE was 1,200+, and I reduced it to ~1,190 after tuning and feature engineering. R² improved to 0.977, showing a solid model fit.

## Challenges Faced

1. **Handling Missing Data**  
   Some columns had significant missing values, especially critical ones like genre. For numerical features, I imputed values, but for categorical ones, I decided to drop rows entirely. Balancing data loss with model performance was tricky.

2. **Outliers**  
   Outliers were skewing the data significantly, especially in numeric fields like salary and debt. I applied Z-score filtering to remove them, which helped stabilize the model predictions.

3. **Feature Engineering**  
   Coming up with the right features like `salary_to_debt_ratio` wasn’t straightforward. I tried different combinations to see what worked best in improving model accuracy.

4. **Tuning LightGBM**  
   Using GridSearchCV to tune hyperparameters was time-intensive but necessary. Striking a balance between computation time and model performance was challenging but worth it in the end.

## Results

- **MAE**: Brought down to ~1,190 after tuning and feature engineering.  
- **R²**: Improved to 0.977, showing that the model is very reliable for this task.  
- **MSE**: Stabilized around 2.46M, indicating fewer extreme errors in predictions.

## How to Use

1. Upload your dataset to Google Colab (or use any other Python environment).  
2. Follow the preprocessing steps to clean and prepare the data.  
3. Train the LightGBM model with the provided code.  
4. Evaluate your results using RMSE and R² metrics.
