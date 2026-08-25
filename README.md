Multiple Linear Regression — Car Price Prediction

A machine learning project that predicts car prices based on multiple vehicle characteristics using Multiple Linear Regression.

Project Overview

This project demonstrates how Multiple Linear Regression can be used to predict a car's price from several features at the same time.

Instead of relying on a single factor such as horsepower, the model considers different characteristics of a vehicle, including engine size, dimensions, fuel type, body style, drivetrain, and other specifications. The project also explores how these variables relate to car prices and evaluates how well the model performs on unseen data.

Dataset
Dataset: Car Price Assignment dataset
Target Variable: price
Original Features: 26 columns
Processed Features: 44 columns after converting categorical variables into numerical features
Observations: 205 cars
Format: CSV

Categorical variables are converted into numerical values so they can be used by the regression model.

Methodology
Approach
Data Loading: Load the car dataset using pandas
Data Exploration: Examine the dataset and visualize relationships between variables
Feature Preparation: Separate the input features from the target price
Categorical Encoding: Convert categorical variables into numerical features
Data Shuffling: Randomize the dataset before modeling
Train-Test Split: Use an 80-20 split for training and testing
Model Training: Fit an Ordinary Least Squares (OLS) regression model
Evaluation: Compare predicted prices with actual prices using R²

The final split contains 164 training observations and 41 test observations.

Model
Multiple Linear Regression

Multiple Linear Regression estimates a target value using several input variables at once.

In this project, the model learns the relationship between vehicle characteristics and car price. The OLS model was trained using statsmodels.

model = sm.OLS(y_train, x_train).fit()
Performance

The model achieved:

Training R²: 0.938
Adjusted R²: 0.917
Test R²: 0.904

The test R² of approximately 0.904 indicates that the model explains a large portion of the variation in car prices on previously unseen data.
The notebook also compares actual and predicted prices to evaluate individual predictions.

Key Libraries
Python 3.x
pandas
scipy
statsmodels
seaborn
matplotlib
scikit-learn
Installation
Clone the repository or download the project files.
Set up a Python virtual environment (recommended).
Install the required packages:
pip install pandas scipy statsmodels seaborn matplotlib scikit-learn jupyter
Usage
Running the Notebook

Open the Jupyter notebook:

jupyter notebook MultipleRegression.ipynb

Run the cells in order to follow the complete workflow:

Data loading and exploration
Data visualization
Feature preparation
Model training
Prediction
Model evaluation
