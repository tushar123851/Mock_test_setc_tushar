# Delivery Risk Prediction

## Data Science & AI/ML Practical Exam — Set c

### Project Overview

This project focuses on predicting late deliveries and identifying
operational segments using Data Science, Machine Learning, Clustering, and
Artificial Neural Networks.

## Objective

The main objectives of this project are:

- Predict whether a delivery will be late.
- Perform statistical analysis on delivery data.
- Prepare and transform the dataset for modeling.
- Build a Logistic Regression model.
- Identify operational segments using K-Means clustering.
- Build an Artificial Neural Network (ANN).

## Dataset

The dataset contains the following columns:

- `record_id` — Unique record identifier
- `distance` — Synthetic distance index
- `load` — Synthetic load index
- `traffic` — Synthetic traffic index
- `staff` — Synthetic staff index
- `group` — Operational group (G1/G2)
- `late` — Target variable (1 = Late, 0 = Not Late)

The generated dataset contains 305 rows including 5 duplicate rows.
After removing duplicates, 300 unique records remain.

## Engineered Feature

An additional feature is created using:

```text
engineered_feature = load / (staff + 1)
```

## Project Tasks

### Task 1 — Maths & Advanced Statistics

- Descriptive Statistics
- Welch T-Test
- Confidence Interval
- Covariance Matrix
- Eigenvalue Analysis

### Task 2 — Data Preprocessing & Feature Engineering

- Duplicate Removal
- Missing Value Handling
- Median Imputation
- One-Hot Encoding
- Feature Engineering
- Standard Scaling
- Train, Validation and Test Splitting

### Task 3 — Supervised Learning

- Dummy Classifier
- Logistic Regression
- Model Evaluation
- Confusion Matrix

### Task 4 — Unsupervised Learning

- K-Means Clustering
- Inertia
- Silhouette Score
- Operational Segmentation

### Task 5 — Artificial Neural Network

- Dense Neural Network
- ReLU Activation
- Sigmoid Output
- Binary Cross-Entropy
- Adam Optimizer
- Early Stopping
- Training and Validation Loss

## Data Split

- Fit Data: 192 records
- Validation Data: 48 records
- Test Data: 60 records
- Random State: 42

## Technologies Used

- Python
- NumPy
- Pandas
- SciPy
- Scikit-learn
- Matplotlib
- TensorFlow / Keras
- Jupyter Notebook

## How to Run

Install the required packages:

```bash
pip install -r requirements.txt
```

Generate the dataset:

```bash
python src/generate_data.py
```




## Author

**Name:** Tushar Vala  
**Student ID:** 10674  
**Set:** c — Delivery Risk

## Declaration

All work is my own except where cited.
