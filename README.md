# Online Shoppers Intention Prediction

[![forthebadge](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![forthebadge](https://img.shields.io/badge/Pandas-brightgreen.svg)](https://pandas.pydata.org/)
[![forthebadge](https://img.shields.io/badge/Scikit--Learn-orange.svg)](https://scikit-learn.org/stable/)
[![forthebadge](https://img.shields.io/badge/Seaborn-lightgrey.svg)](https://seaborn.pydata.org/)
[![forthebadge](https://img.shields.io/badge/Matplotlib-lightgrey.svg)](https://matplotlib.org/)

## What it does

This project aims to predict whether a website visitor will make a purchase during their online session. By analyzing various features related to user behavior, such as the types of pages visited, the time spent on them, bounce rates, and more, the model learns to classify sessions as either leading to revenue (a purchase) or not.

## Why it matters

Understanding and predicting which online sessions are likely to result in a purchase is valuable for several reasons:

* **Business Optimization:** E-commerce businesses can use these predictions to optimize their strategies. For example, they can identify high-potential customers and offer them personalized promotions or improve their user experience to encourage conversion.
* **Resource Allocation:** Marketing efforts and website resources can be focused on users who are more likely to make a purchase, leading to more efficient spending.
* **Customer Understanding:** Analyzing the features that are strong predictors of purchase intention can provide valuable insights into customer behavior and preferences.

## How I approached it

The approach to this project involved several key steps:

1.  **Data Exploration and Preprocessing:**
    * Loading and understanding the dataset containing online shopping session information.
    * Handling categorical features (like visitor type and month) by converting them into a numerical format that machine learning models can understand (using One-Hot Encoding).
    * Converting boolean features (like weekend and revenue) into numerical representations (0 and 1).
    * Scaling numerical features to ensure that models are not biased by the different scales of the input variables.

2.  **Model Selection and Training:**
    * Initially, a **Logistic Regression** model was explored for its simplicity and interpretability in binary classification tasks.
    * Recognizing potential issues with **class imbalance** (where 'No Purchase' sessions significantly outnumbered 'Purchase' sessions), techniques like `class_weight='balanced'` were used to make the model pay more attention to the minority class.
    * **Tree-based models**, such as **Random Forest**, were also considered and might be a preferred choice in a real-world scenario due to their ability to handle non-linear relationships and their robustness against overfitting. Overfitting, where a model learns the training data too well and performs poorly on new data, was a key concern.

3.  **Evaluation:**
    * The trained models were evaluated on a separate test dataset to assess their ability to generalize to new, unseen data.
    * Metrics such as **accuracy**, **precision**, **recall**, and the **F1-score** were used to understand the model's performance, particularly in predicting the less frequent 'Purchase' outcome.
    * **Confusion matrices** were used to visualize the model's predictions and identify areas for improvement, such as reducing false positives and false negatives.

This project demonstrates a standard machine learning workflow for a classification problem, highlighting the importance of data preprocessing, model selection, handling class imbalance, and thorough evaluation.
