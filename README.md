# Fraud Detection Project

A machine learning project for detecting fraudulent transactions using Support Vector Machine (SVM) classification.

## Overview

This project implements a fraud detection system that analyzes transaction data to identify potentially fraudulent activities. The model uses various transaction features to predict whether a transaction is legitimate or fraudulent.

## Features

- Data preprocessing and feature engineering
- Label encoding for categorical variables
- Support Vector Machine (SVM) classification
- Model evaluation with accuracy metrics
- Data visualization with pie charts

## Dataset

The project uses transaction data with the following features:
- Transaction amount
- Merchant information
- Category of transaction
- Customer demographics (gender, job)
- Transaction timestamp and location data

## Requirements

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

## Usage

1. Load the dataset (`fraudTest.csv`)
2. Run data preprocessing steps
3. Train the SVM model
4. Evaluate model performance
5. Make predictions on test data

## Model Performance

The SVM model achieves high accuracy on the fraud detection task. The dataset shows class imbalance with the majority of transactions being legitimate.

## Files

- `fraud_detection.ipynb`: Main Jupyter notebook with the complete analysis
- `fraudTest.csv`: Dataset file (not included in repository)

## Installation

1. Clone this repository
2. Install required packages: `pip install pandas numpy matplotlib seaborn scikit-learn`
3. Run the Jupyter notebook

## Author

Abhishek Joshi