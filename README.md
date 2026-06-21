# Customer Segmentation and Churn Prediction Using Machine Learning

## Project Topic
This project investigates customer behavior within the telecommunications industry, utilizing both unsupervised and supervised machine learning techniques to segment customers and predict service cancellation (churn).

## Main Objective
To uncover distinct customer profiles using K-Means clustering, and to build robust classification models (Logistic Regression and Random Forest) capable of identifying high-risk customers before they churn.

## Project Type
This project is structured as a **Technical Report**. It combines business problem formulation, mathematical algorithm explanations, Python code, and predictive data modeling in a Jupyter Notebook.

## Methodology
1. **Exploratory Data Analysis (EDA):** Investigated distributions, class imbalances, and feature relationships (e.g., tenure vs. churn).
2. **Feature Engineering:** Applied one-hot encoding for categorical variables and `StandardScaler` for numeric features to prepare data for distance-based algorithms.
3. **Unsupervised Learning (Clustering):** Utilized the Elbow Method to determine optimal clusters ($k=3$) and applied K-Means to segment the customer base into distinct behavioral profiles.
4. **Supervised Learning (Classification):** Addressed class imbalance using stratified train/test splitting and balanced class weights. Trained a Logistic Regression baseline and a Random Forest Classifier to predict the binary `Churn` target.
5. **Mathematical Evaluation:** Evaluated models by prioritizing **Recall** to capture maximum at-risk customers, and visualized performance using Confusion Matrices and Feature Importance charts.

## Repository Structure
- `data/` — Contains the original Telco Customer Churn dataset.
- `notebooks/` — Contains the main Jupyter Notebook (`churn_prediction_analysis.ipynb`).