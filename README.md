# Machine Learning Classification of Breast Cancer Tumors

## Overview

This project applies several supervised machine learning models to the **Wisconsin Diagnostic Breast Cancer (WDBC)** dataset. The goal is to classify tumors as benign or malignant based on measured cell features. This pipeline includes data preprocessing, feature selection, model training, hyperparameter tuning, and performance evaluation.

---

## Objectives

* Explore and visualise the WDBC dataset
* Build multiple classification models: k-NN, Decision Tree, SVM, and Naive Bayes
* Compare models based on accuracy, precision, recall, and confusion matrices
* Identify the best-performing model for tumor classification

---

## Dataset

* **Source:** UCI Machine Learning Repository – Wisconsin Diagnostic Breast Cancer
* **Features:** 30 continuous cell features (mean, standard error, worst)
* **Target:** Diagnosis (`B` for benign, `M` for malignant)

---

## Models Implemented

* **k-Nearest Neighbours (k-NN)**

  * Optimal k determined via accuracy testing across values 1–30
  * Final model achieved **97.37% accuracy**

* **Support Vector Machine (SVM)**

  * Explored linear and radial kernels
  * Tuned cost parameter to control margin width

* **Decision Tree Classifier**

  * Evaluated overfitting vs underfitting
  * Visualised tree structure and class splits

* **Naive Bayes**

  * Used as a baseline probabilistic classifier
  * Fast and interpretable, but underperformed vs others

---

## Key Results

| Model         | Accuracy | Notes                               |
| ------------- | -------- | ----------------------------------- |
| k-NN (k=7)    | 97.37%   | Best performer, minimal overfitting |
| Decision Tree | \~93%    | Slightly lower, interpretable tree  |
| SVM (linear)  | \~94–96% | Highly stable, robust performance   |
| Naive Bayes   | \~89%    | Simplest, lowest performance        |

* k-NN achieved best test accuracy while remaining robust to noise
* SVM showed consistently high results with well-separated classes
* Decision Tree offered the most interpretability but with some overfitting

---

## Tools Used

* **Language:** R
* **Libraries:** `caret`, `class`, `e1071`, `rpart`, `ggplot2`, `dplyr`
* **Environment:** RStudio, Quarto Notebook (`.qmd`)

---

## File Contents

* `LIFE748_ML-TEST_FINAL.qmd`: Full machine learning analysis notebook
* `annotated-LIFE748_ML-TEST_FINAL.pdf`: Instructor-annotated version with feedback
* `wdbc.csv`: (Add if including dataset locally)
* `plots/`: Contains generated graphs and model visualisations

---

## Notes

* Data split into 70% training / 30% testing sets
* k-NN model used standardised features to reduce feature scale bias
* All models evaluated using confusion matrix and accuracy metrics
