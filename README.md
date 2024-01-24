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

## Decision Tree

* The 'price' column was separated as the target variable ('y'), and the remaining columns were used as features ('X').
  
* The dataset was split into training and testing sets using the train_test_split function.

* Standard scaling was applied to the features using StandardScaler to normalize the data.

* A Decision Tree Regressor model was created with the parameters: `Max_Depth = 15` and `random_state = 0`.

* Once the model was trained and used to predict the test values, the model results were:
  * R2 Score = 0.93
  * MSE = 6128960.49

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

* If we had the opportunity to repeat this project, we would use live API data to build the model on real-time data

* Additionally, we could have used the mean squared error metric across all models to work out absolute error. 

* It would also be good to use cross validation techniques to help gauge how well the model works with unseen data 

## References

| Reference Name | Description |
| -------------- | ----------- |
| [Kaggle.com](https://www.kaggle.com/datasets/adityadesai13/used-car-dataset-ford-and-mercedes) | Used Car Dataset |
| [Scikit-Learn.org](https://scikit-learn.org/stable/) | Python library to create, train, test, and evaluate Machine Learning Models |
| [edX](https://www.edx.org/) | Data Bootcamp provider and Project Requirements definition |
