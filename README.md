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
3. **Unsupervised Learning (Clustering):** Utilized the Elbow Method to determine optimal clusters ($k=4$) and applied K-Means to segment the customer base into distinct behavioral profiles.
4. **Supervised Learning (Classification):** Addressed class imbalance using stratified train/test splitting and balanced class weights. Trained a Logistic Regression baseline and a Random Forest Classifier to predict the binary `Churn` target.
5. **Mathematical Evaluation:** Evaluated models by prioritizing **Recall** to capture maximum at-risk customers, and visualized performance using Confusion Matrices and Feature Importance charts.

## Random Forest Results

The Random Forest model achieved the following results on the test set:

* **Accuracy:** 77%
* **Churn Precision:** 55%
* **Churn Recall:** 74%
* **Churn F1-score:** 63%

The model successfully identifies a large portion of customers who actually churn, which is valuable for a retention-focused business use case. However, the precision score shows that some customers are incorrectly flagged as churn risks, meaning future work could focus on improving the precision-recall tradeoff.

## Key Findings

* K-Means clustering identified **four distinct customer segments**, showing that churn behavior differs across customer groups.
* Random Forest achieved strong churn recall, making it useful for identifying customers who may need retention actions.
* Important churn drivers include customer tenure, contract type, monthly charges, and related account/service characteristics.

## Repository Structure

* `data/` — Contains the Telco Customer Churn dataset.
* `notebooks/` — Contains the main Jupyter Notebook: `churn_prediction_analysis.ipynb`.
* `README.md` — Project overview, methodology, results, and repository instructions.

## Future Work

Future improvements could include hyperparameter tuning with GridSearchCV or RandomizedSearchCV, testing boosting algorithms such as XGBoost or LightGBM, and experimenting with different probability thresholds to optimize the balance between precision and recall.