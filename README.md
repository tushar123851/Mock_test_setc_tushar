# Machine Quality Prediction

## Data Science & AI/ML Practical Exam — Set C

### Project Overview

This project focuses on predicting defective production batches and identifying
operating regimes using Data Science, Machine Learning, Clustering, and
Artificial Neural Networks.

## Objective

The main objectives of this project are:

- Predict whether a production batch will be defective.
- Perform statistical analysis on machine quality data.
- Prepare and transform the dataset for modeling.
- Build a Logistic Regression model.
- Identify operating regimes using K-Means clustering.
- Build an Artificial Neural Network (ANN).

## Dataset

The dataset contains the following columns:

- `record_id` — Unique record identifier
- `temperature` — Synthetic temperature index
- `vibration` — Synthetic vibration index
- `pressure` — Synthetic pressure index
- `hours` — Synthetic operating hours index
- `group` — Operational group (G1/G2)
- `defect` — Target variable (1 = Defect, 0 = No Defect)

The generated dataset contains 305 rows including 5 duplicate rows.
After removing duplicates, 300 unique records remain.

## Engineered Feature

An additional feature is created using:

```text
engineered_feature = vibration * pressure
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
- Operating Regime Identification

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

Then open and run:

```text
notebooks/exam.ipynb
```

## Author

**Name:** Tushar Vala  
**Student ID:** 10674  
**Set:** C — Machine Quality

## Declaration

All work is my own except where cited.
