#  Predicting Video Game Sales Hits

This project uses machine learning to predict whether a video game will be a **sales hit (over 1 million copies sold)** based on early features such as platform, genre, publisher, and rating — without relying on user or critic scores.

---

##  Project Overview

- **Goal:** Predict if a video game will be a commercial hit using classification.
- **Why it matters:** Helps game publishers make early decisions about marketing, budgeting, and platform targeting.
- **Approach:** Framed as a binary classification problem ("Hit" vs. "Not Hit").

---

##  Business Problem

> *Can we predict whether a video game will be a sales hit based only on features available before launch — like genre, platform, publisher, and rating?*

---

##  Dataset

- Source: Merged from two Kaggle datasets
- Size: ~59,000 records
- Key columns:
  - `Platform`, `Genre`, `Publisher`, `Rating`
  - `Global_Sales`, `NA_Sales`, `EU_Sales`, etc.
  - `Year_of_Release`, `Critic_Score`, `User_Score` (not used due to missing values)

---

##  Data Cleaning

- Removed duplicates and games with missing critical fields
- Grouped rare genres and publishers under "Other"
- Converted `Year_of_Release` to integer
- Dropped `Critic_Score`, `User_Score` due to too many nulls

---

##  Feature Engineering

- Created binary target: `is_hit` (1 if global sales > 1M, else 0)
- One-hot encoded categorical features
- Dropped non-predictive fields like game name and developer

---

##  Modeling

- Models used:
  - Logistic Regression (baseline)
  - Random Forest Classifier ✅ (best performance)
  - XGBoost
- Train/test split: 80/20
- Final evaluation metric: Accuracy and confusion matrix

---

##  Key Insights

- Most games sell fewer than 1 million copies
- Platform, genre, and publisher are the top predictors
- Mature-rated games tend to have higher average sales than child-friendly ones
- Release year trends (e.g., 2009–2012 drop, post-2019 decline) give valuable context

---

##  Future Work

- Incorporate user reviews and search trend data
- Try deep learning on game descriptions
- Train regression models to estimate exact sales volume

---

##  License

This project is for educational purposes. Data sourced from Kaggle.

---

