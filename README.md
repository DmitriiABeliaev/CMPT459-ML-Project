# COVID-19 Medical Outcome Prediction

A machine learning project aimed at predicting COVID-19 patient outcomes using cleaned and preprocessed global COVID-19 data. Developed as part of CMPT 459 - Data Mining and Data Warehousing.

## Problem Statement
Analyzed incomplete COVID-19 datasets across continents to develop predictive models. Addressed major data inconsistencies, particularly from underrepresented regions like Africa and Asia.

## Data Preprocessing
Key preprocessing operations of Data Preprocessing:
- **Data Cleaning:** Standardized country names, handled missing values, corrected invalid entries.
- **Feature Mapping:** Created meaningful features such as "expected mortality rate" and encoded proper value types to features like "sex" and "chronic disease binary".
- **Dataset Merging:** Combined location and patient outcome datasets, aggregating duplicates.
- **Class Balancing:** Applied SMOTENC oversampling to address class imbalance in target variables. Resulted in increased dataset size from 17,212 to 60,096 entries, with evenly distributed target classes.

Ex: Before and After the Class Balancing

![Image](https://github.com/user-attachments/assets/c49636e3-4696-4d97-b7a1-0441731c4050)

## Model Development
Developed and evaluated four machine learning models:
- **Logistic Regression**
  Great for interpretability, tuned for C and penalty.
- **K-Nearest Neighbors**
  Fast training, ideal for non-noisy balanced data.
- **Gradient Boosting Classifier**
  High accuracy, especially good on complex patterns.
- **Random Forest**
  Best performer, robust and low overfitting.

**Hyperparameter Tuning**:  
- GridSearchCV for Logistic Regression, KNN, Gradient Boosting.
- RandomizedSearchCV for Random Forest.

![Image](https://github.com/user-attachments/assets/f612f9f3-ee8e-45a8-ba0e-673d6937e34a)

**Cross-validation:**  
- 5-Fold Cross Validation to assess model generalization and detect overfitting.
- All models showed very low variance between training and validation accuracy (≤ 0.02).
- Random Forest and KNN had highest train accuracy; Logistic Regression had least variance.

**Overfitting Checks:** 
- Compared train vs. validation accuracy.
- Regularization (L1/L2), tuning max_depth, min_samples_leaf, and C mitigated overfitting risks.


## Results
- Random Forest achieved the best F1-scores and accuracy with minimal overfitting.
- Class distributions were balanced post-SMOTENC application.
- Models demonstrated robust performance even on unseen (unlabeled) data.
- For more details of our work process and finding check report.pdf

## Build Instructions
- Clone the Repository
- Set Up a Python Environment (using venv or conda)
- Install Required Packages (pip install -r requirements.txt)
- Run the Code

## Build Instructions
- SMOTE-ENC for Mixed Data: https://arxiv.org/ftp/arxiv/papers/2103/2103.07612.pdf
- Tree Models vs. Deep Learning: https://arxiv.org/abs/2207.08815
- KNN Algorithm Guide: https://neptune.ai/blog/knn-algorithm-explanation-opportunities-limitations

## Team Contributions
- Dmitrii Beliaev
- Tristian Labanowich
- Long Duong
- Manvir Singh Heer
