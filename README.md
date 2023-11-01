# Credit Risk Classification

## Overview

This repository contains the work of a machine learning project aimed at predicting credit risk. Financial institutions rely on risk assessment to make informed loan approval decisions. This project leverages historical lending data from a peer-to-peer lending services company to build a logistic regression model that classifies the risk associated with new borrowers. The objective is to minimize the risk of defaults by accurately identifying high-risk loans.


## Project Structure

```
credit-risk-classification/
│
├── Credit_Risk/
│   ├── credit_risk_classification.ipynb  # Jupyter notebook with analysis
│   └── lending_data.csv                  # Dataset used for model training and testing
│
├── README.md                             # Project overview and results
└── .gitignore                            # Specifies intentionally untracked files to ignore
```

## Methodology

The project follows a standard machine learning pipeline:

1. **Data Preprocessing**: The `lending_data.csv` dataset is read into a Pandas DataFrame. Features and labels are then separated for the modeling process.

2. **Model Training and Testing**: The data is split into training and testing sets. A logistic regression model is trained with the original data.

3. **Resampling**: Due to class imbalance in the training data, RandomOverSampler is used to oversample the minority class in the dataset.

4. **Model Evaluation**: The model's performance is evaluated using metrics such as accuracy, precision, and recall scores.

## Results

The analysis included two machine learning models:

- **Model 1**: Original data without resampling.
  - Accuracy: 94%
  - Precision for high-risk loans: 87%
  - Recall for high-risk loans: 89%

- **Model 2**: Data with oversampling.
  - Accuracy: 99%
  - Precision for high-risk loans: 87%
  - Recall for high-risk loans: 100%

Model 2, with resampled data, demonstrated superior performance and is recommended for identifying high-risk loans due to its perfect recall score.

## Installation

To set up a local development version, follow these steps:

```bash
# Clone the repository
git clone https://github.com/LevanGetia/credit-risk-classification.git

# Navigate to the project directory
cd credit-risk-classification
```

## Usage

To run the Jupyter notebook:

```bash
# Navigate to the Credit_Risk directory
cd Credit_Risk

# Start the Jupyter notebook
jupyter notebook credit_risk_classification.ipynb
```

