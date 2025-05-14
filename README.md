# Video Game Sales Prediction Project

## Overview

This project explores whether it's possible to predict the commercial success of a video game based on its genre, platform, release year, and publisher. Using machine learning, we aim to answer two key questions:

1. **Classification**: Will the game sell more than 1 million units globally?  
2. **Regression**: How many millions of units will the game sell globally?

Additionally, we explore which features (e.g., genre, score, platform) are most predictive of strong regional sales in North America (NA), Europe (EU), and Japan (JP).

## Business Problem

The global gaming market is highly competitive. Understanding the factors that influence game sales can help publishers make better strategic decisions. This project aims to develop predictive models that classify whether a game will be a sales hit, as well as estimate expected global sales volume.

## Dataset

The dataset used in this project includes:
- Game title, platform, and release year
- Publisher and genre
- Global and regional sales (NA, EU, JP)
- Critic and user scores

The cleaned dataset used for modeling is available in this repository: `video_game_sales_final_cleaned.csv`.

## Objectives

- Predict whether a game will be a global hit (1M+ copies sold) using classification models
- Predict exact global sales in millions using regression models
- Identify the most important features influencing sales in global and regional markets

## Features Used

- Genre
- Platform
- Publisher
- Release Year
- Critic Score
- User Score

## Project Structure

- `eda/` - Exploratory data analysis and visualizations
- `models/` - Machine learning models for classification and regression
- `notebooks/` - Jupyter notebooks for development and experimentation
- `video_game_sales_final_cleaned.csv` - Cleaned dataset used in this project
- `README.md` - Project overview and guide

## Methodology

1. Data Cleaning and Preprocessing
   - Missing value handling
   - One-hot encoding for categorical features
   - Feature selection

2. Modeling
   - **Classification**: Random Forest, Logistic Regression, XGBoost
   - **Regression**: Random Forest Regressor, XGBoost Regressor

3. Model Evaluation
   - Accuracy, precision, recall for classification
   - RMSE, MAE for regression
   - Cross-validation and GridSearchCV for hyperparameter tuning

4. Feature Importance Analysis
   - Visualizations of top predictive features
   - Region-specific model insights (NA, EU, JP sales prediction)

## Results

- The classification model achieved high accuracy in identifying global hits.
- Regression models were effective in approximating total sales volume.
- Genre, platform, and critic score were consistently among the most predictive features.

## How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/video-game-sales-prediction.git
   cd video-game-sales-prediction
