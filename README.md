# Loan Approval Prediction

## Overview

This project builds a machine learning model to predict whether a loan application will be **approved (1)** or **declined (0)** based on customer demographic and financial information.

Using historical loan application data, several classification models were trained and evaluated to identify patterns that influence loan approval decisions. The models are trained on the provided **training dataset** and used to generate predictions for the **test dataset**.

Multiple algorithms were explored, including:

- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- Neural Network (TensorFlow/Keras)

The final predictions are formatted according to the required Kaggle submission structure.

---

## Dataset

The project uses three CSV files:

- **train.csv** – Training data containing features and the target variable (`loan_status`)
- **test.csv** – Unlabeled dataset used for generating predictions
- **sample_submission.csv** – Example file showing the correct submission format

### Features

The dataset includes the following attributes:

- `person_age`
- `person_gender`
- `person_education`
- `person_income`
- `person_emp_exp`
- `person_home_ownership`
- `loan_amnt`
- `loan_intent`
- `loan_int_rate`
- `loan_percent_income`
- `cb_person_cred_hist_length`
- `credit_score`
- `previous_loan_defaults_on_file`
- `loan_status` (Target variable)
- `loan_id`

---

## Methodology

1. Load training and testing datasets.
2. Encode categorical variables using **one-hot encoding**.
3. Align train and test feature columns.
4. Standardize numerical features using **StandardScaler**.
5. Split training data into **training and validation sets**.
6. Train multiple classification models.
7. Evaluate models using **accuracy**.
8. Generate predictions for the test dataset.

---

## Submission Format

Predictions must follow this format:
loan_id,loan_status
2,0
5,1
6,0

- `loan_id` – ID from the test dataset
- `loan_status` – Predicted outcome (**1 = Approved, 0 = Declined**)
