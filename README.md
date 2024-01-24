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

## Random Forest Regression

## Model Comparison/Conclusion 

![image](https://github.com/DarrylHewitt/Project_4/assets/136898379/5df0f0fa-ad80-408a-a0b3-1258fdcb0490)

## Reflections/Evaluation
