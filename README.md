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

## Visualisation
![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/f6a0e0a2-ee60-4d60-814c-fd6e7cbca413)
To get a better idea of the data set we used a correlation matrix.

Before building any machine learning model we looked at which variables are correlated, to can gain a better understanding about what’s most important for our models.

Price measure against engine size and year of the car showed a positive relationship.

Price measure against mpg and mileage showed a negative relationship.

![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/d7bd6bd9-c29f-4def-87b1-cc758865494b)
![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/2285b8fe-93b3-4fcf-bf37-ad287c4a35db)

To enhance the representation of data variation, a violin plot was employed. Notably, both automatic and semi-auto transmissions exhibit higher mean prices, accompanied by instances of extreme prices. The make of the car is also a critical factor in this analysis

![image](https://github.com/DarrylHewitt/Project_4/assets/140830640/be56a3e1-b540-4e44-92a3-952678ed6c27)

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

  <img width="193" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/d6ee20fd-39c7-4530-9f76-5e27862f493f">

* The model was used to make predictions on the test set, and a DataFrame was created to compare predicted and actual values.

  <img width="326" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/1777daae-06a6-42a6-bd5b-d4451bffc875">

* The importance of each feature in making predictions was determined using the Random Forest model, and the top 10 features were identified.

  <img width="663" alt="image" src="https://github.com/DarrylHewitt/Project_4/assets/136898379/a1ae0978-a812-4982-99f8-a880a31a8a18">

## Model Comparison/Conclusion 

![image](https://github.com/DarrylHewitt/Project_4/assets/136759285/7bb354fb-9a3b-45e1-afc7-e4b88f702fda)

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
