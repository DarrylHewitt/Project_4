# Project Overview

The goal of this project was to develop several predictive models for used car prices. We used a dataset with features such as model, year, transmission, mileage, fuel type, and engine size, to uncover patterns and relationships influencing the pricing of used cars.

## The Dataset 

Link: https://www.kaggle.com/datasets/adityadesai13/used-car-dataset-ford-and-mercedes 

The original dataset had been extracted from 100,000 used car listings and then organized into individual files corresponding to each distinct car manufacturer. 

## Data Cleaning

* The separate files were pooled into a unified dataset and an additional column was included specifying the car's make.

  <img width="691" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/5ae2d2c5-1a2b-4bbf-bc1f-e204502a5a4a">

* A check was conducted for any missing values.

  <img width="255" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/e7ccd36b-e45e-4eb2-a5be-7c71927ffb3c">

* A quick statistical analysis was run using .describe() to spot outliers and potential errors.

  <img width="460" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/ffe4fb40-2129-448d-87fb-48536210455c">

* The refined dataset was then saved into a fresh CSV for easy access.

  <img width="342" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/eb6dcfd1-6b11-4497-931c-ef56cccd8515">

## The Database

A SQLite database was used to store the dataset. The data from the CSV file was read into a Pandas DataFrame and then committed to a newly-created SQLite database. 

<img width="387" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/80e95796-89f8-4ad4-8841-0b106e7aea4f">

## PCA

## Random Sample Consensus - RANSAC 
![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/f365dc11-131a-44ba-9dda-83088c234dbb)
Predicting Car Prices with RANSACRegressor
Data Preparation:
Extracted features (X) from 'cars_sold_df,' excluding the 'price' column.
Set the target variable (y) to the 'price' column.
Handling Categorical Variables:
Identified and one-hot encoded categorical columns in X.
Train-Test Split:
Split the dataset into training (80%) and testing (20%) sets.
Ensured reproducibility with random_state=42.
Model Initialization and Training:
Initialized a RANSACRegressor model with a maximum of 100 trials.
Trained the model on the training data.
Result:
Obtained a trained RANSACRegressor model capable of predicting car prices, considering potential outliers.
![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/f00dc5c9-c446-4c92-a0e8-2a38e235e7b8)
Model Training:
Used RANSACRegressor with default settings on the training data.
Prediction and Evaluation:
Made predictions on the testing set.
Evaluated using metrics: MAE, MSE, RMSE, R2.
Results:
Predicted car prices on the testing set and key evaluation metrics.
Interpretation:
Interpreted metrics: MAE, MSE, RMSE, R2 for understanding model performance.
![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/f9048030-09d6-434e-a9d7-f430b77aef19)

Model Training:
Used RANSACRegressor with default settings on the training data.
Prediction and Evaluation:
Made predictions on the testing set.
Evaluated using metrics: MAE, MSE, RMSE, R2.
Results:
Predicted car prices on the testing set and key evaluation metrics.
Interpretation:
Interpreted metrics: MAE, MSE, RMSE, R2 for understanding model performance.
![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/b4254f4a-f8d8-44c3-8946-06f87f4cb8bd)
Prediction and Visualization:
Made predictions on the testing set.
Visualized results with a scatter plot, highlighting inliers and the RANSAC regression line.
Check Data Sizes:
Displayed sizes of the testing set and corresponding target variable.
Outcome:
Effectively demonstrated the model's handling of outliers through visualized results.

## Decision Tree

## Random Forest Regression

* The 'price' column was separated as the target variable ('y'), and the remaining columns were used as features ('X').
  
* The dataset was split into training and testing sets using the train_test_split function.

* Standard scaling was applied to the features using StandardScaler to normalize the data.

* A Random Forest Regressor was trained on the scaled training data with specified hyperparameters (50 estimators, max depth of 15).

* The R-squared score was calculated on the scaled test data, resulting in a high value of 0.95, indicating a good fit. Mean Squared Error (MSE) was also calculated, yielding a value of approximately 4.95 million.

* The model was used to make predictions on the test set, and a DataFrame was created to compare predicted and actual values.

* The importance of each feature in making predictions was determined using the Random Forest model, and the top 10 features were identified.

## Model Comparison/Conclusion 

![image](https://github.com/DarrylHewitt/Project_4/assets/136898379/5df0f0fa-ad80-408a-a0b3-1258fdcb0490)

## Reflections/Evaluation

## References

| Reference Name | Description |
| -------------- | ----------- |
| [Kaggle.com](https://www.kaggle.com/datasets/adityadesai13/used-car-dataset-ford-and-mercedes) | Used Car Dataset |
| [Scikit-Learn.org](https://scikit-learn.org/stable/) | Python library to create, train, test, and evaluate Machine Learning Models |
| [edX](https://www.edx.org/) | Data Bootcamp provider and Project Requirements definition |
