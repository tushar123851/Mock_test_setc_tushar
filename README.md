# Delivery Risk Prediction

## Data Science & AI/ML Practical Exam — Set C

### Project Overview

This project focuses on predicting late deliveries and identifying
operational segments using Data Science, Machine Learning, Clustering,
and Artificial Neural Networks.

## Objective

The main objectives of this project are:

- Predict whether a delivery will be late.
- Perform statistical analysis on delivery data.
- Clean and preprocess the dataset.
- Create an engineered feature.
- Build a Logistic Regression model.
- Identify operational segments using K-Means clustering.
- Build an Artificial Neural Network (ANN).
- Evaluate the models using classification metrics.

## Dataset

The dataset contains the following columns:

- `record_id` — Unique record identifier
- `distance` — Synthetic distance index
- `load` — Synthetic load index
- `traffic` — Synthetic traffic index
- `staff` — Synthetic staff index
- `group` — Operational group (G1/G2)
- `late` — Target variable (1 = Late, 0 = Not Late)

The generated dataset contains 305 rows, including 5 exact duplicate rows.

After removing duplicates:

- Total unique records: 300

## Engineered Feature

The following additional feature is created after numeric imputation:

```text
engineered_feature = load / (staff + 1)
```

## Data Split

The dataset is divided using stratified splitting with `random_state=42`.

- Fit Data: 192 records
- Validation Data: 48 records
- Test Data: 60 records
- Random State: 42

## Project Tasks

### Task 1 — Maths & Advanced Statistics

- Descriptive Statistics
- Welch Two-Sample T-Test
- 95% Confidence Interval
- Covariance Matrix
- Eigenvalue Analysis

### Task 2 — Data Preprocessing & Feature Engineering

- Duplicate Removal
- Missing Value Analysis
- Median Imputation
- One-Hot Encoding
- Feature Engineering
- Standard Scaling
- Fit, Validation and Test Splitting
- Data Leakage Prevention

### Task 3 — Supervised Learning

The following models are used:

- Dummy Classifier
- Logistic Regression

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Task 4 — Unsupervised Learning

K-Means clustering is used to identify operational segments.

The following cluster values are evaluated:

```text
k = 2, 3, 4
```

The best number of clusters is selected using the Silhouette Score.

### Task 5 — Artificial Neural Network

The ANN contains:

- Input Layer
- Dense Layer — 16 neurons with ReLU
- Dense Layer — 8 neurons with ReLU
- Output Layer — 1 neuron with Sigmoid

Training configuration:

- Loss Function: Binary Cross-Entropy
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 16
- Maximum Epochs: 50
- Early Stopping Patience: 5
- Classification Threshold: 0.5

## Final Model Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 83.33% | 85.19% | 79.31% | 82.14% |
| Dummy Classifier | 51.67% | 0.00% | 0.00% | 0.00% |
| ANN | 75.00% | 75.00% | 72.41% | 73.68% |

## Key Findings

- Logistic Regression achieved an accuracy of **83.33%** and an F1 Score of **82.14%**.
- ANN achieved an accuracy of **75.00%** and an F1 Score of **73.68%**.
- The Dummy Classifier achieved an accuracy of **51.67%** but an F1 Score of **0.00%**.
- Based on the test F1 Score, Logistic Regression performed better than the ANN for this dataset.

## False Positive and False Negative

### False Positive

A delivery that would actually be **on time** is predicted as **late**.

This may cause unnecessary preventive actions, such as additional staff,
route changes, or other operational adjustments.

### False Negative

A delivery that would actually be **late** is predicted as **not late**.

This may cause the company to miss the opportunity to take preventive
action before the delivery is delayed.

## Technologies Used

- Python
- NumPy
- Pandas
- SciPy
- Scikit-learn
- Matplotlib
- TensorFlow / Keras
- Jupyter Notebook

## Project Structure

```text
MOCK_TEST_SETC_TUSHAR/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── src/
│   └── generate_data.py
│
├── data/
│   └── raw/
│       └── set_b.csv
│
├── notebooks/
│   └── exam.ipynb
│
├── outputs/
│   ├── splits.csv
│   └── figures/
│
└── models/
```

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

Run all notebook cells from top to bottom.

## Limitation

The dataset contains synthetic practice observations and uses a single
small holdout test set. Therefore, the results should not be considered
evidence of causation or deployment readiness.

## Video Explanation

**Video Link:** [Add Your Video Link]  
**Duration:** [Add Video Duration]

## Author

**Name:** Tushar Vala  
**Student ID:** 10674  
**Set:** C — Delivery Risk

## Declaration

All work is my own except where cited.
