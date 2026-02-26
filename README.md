# Customer Churn Prediction in Telecom Industry

**Team:** 24ADI004 — DSV Team 11 | **Course:** Data Science & Visualization — Semester 4

---

## Project Overview

This project uses the **Telco Customer Churn Dataset**, which contains customer information from a telecommunications service provider. The dataset is designed to help analyze customer behavior and understand the factors that influence customer churn.

## Dataset Description

### Basic Information
- **Total Records**: 7,043 customer records
- **Total Attributes**: 21 features
- **Target Variable**: `Churn` (Yes/No)
- **Data Source**: `WA_Fn-UseC_-Telco-Customer-Churn.csv`

Each row in the dataset represents a unique customer with their demographic details, service subscriptions, account information, and billing data.

## Target Variable

**Churn**: Indicates whether a customer has discontinued the service
- `Yes`: Customer has left the service
- `No`: Customer continues with the service

## Feature Categories

The features in the dataset can be broadly categorized into four main groups:

### 1. Demographic Information
- `gender`: Customer's gender (Male/Female)
- `SeniorCitizen`: Whether the customer is a senior citizen (1/0)
- `Partner`: Whether the customer has a partner (Yes/No)
- `Dependents`: Whether the customer has dependents (Yes/No)

### 2. Service Usage Details
- `PhoneService`: Whether the customer has phone service (Yes/No)
- `MultipleLines`: Whether the customer has multiple lines (Yes/No/No phone service)
- `InternetService`: Type of internet service (DSL/Fiber optic/No)
- `OnlineSecurity`: Whether the customer has online security (Yes/No/No internet service)
- `OnlineBackup`: Whether the customer has online backup (Yes/No/No internet service)
- `DeviceProtection`: Whether the customer has device protection (Yes/No/No internet service)
- `TechSupport`: Whether the customer has tech support (Yes/No/No internet service)
- `StreamingTV`: Whether the customer has streaming TV (Yes/No/No internet service)
- `StreamingMovies`: Whether the customer has streaming movies (Yes/No/No internet service)

### 3. Account Information
- `customerID`: Unique identifier for each customer
- `tenure`: Number of months the customer has stayed with the company
- `Contract`: Type of contract (Month-to-month/One year/Two year)
- `PaperlessBilling`: Whether the customer has paperless billing (Yes/No)

### 4. Billing Information
- `PaymentMethod`: Method of payment (Electronic check/Mailed check/Bank transfer/Credit card)
- `MonthlyCharges`: The amount charged to the customer monthly (numerical)
- `TotalCharges`: The total amount charged to the customer (numerical)

## Data Types

The dataset includes both **categorical** and **numerical** variables:

### Categorical Features
Most features in the dataset are categorical, including:
- Binary features (Yes/No, Male/Female)
- Multi-class features (Contract types, Internet service types, Payment methods)

### Numerical Features
- `tenure`: Customer subscription duration (in months)
- `MonthlyCharges`: Monthly billing amount
- `TotalCharges`: Total billing amount over the customer's lifetime

## Analysis Workflow

The Jupyter notebook (`Telecom_Churn.ipynb`) includes the following analysis steps:

1. **Data Loading**: Import the dataset using pandas
2. **Data Exploration**: 
   - View first and last records
   - Check data types and information
   - Generate descriptive statistics
3. **Data Quality Checks**:
   - Check for missing values
   - Check for duplicate records
   - Analyze unique values in each column

## Weekly Progress

**Week 2 — Data Loading**
- Loaded and explored the dataset
- Checked nulls, data types, and descriptive stats
- Converted `TotalCharges` to numeric

**Week 3 — Data Cleaning**
- Filled missing values: numerical → median, categorical → mode
- Outlier detection using boxplots and Z-score (no outliers found)

**Week 4 — EDA**
- Churn distribution pie chart (~26% churn rate)
- Demographic and service usage vs churn plots
- Correlation heatmap for numerical features

---

## Key Findings

- ~26% of customers have churned
- Shorter tenure and higher monthly charges → higher churn
- Gender has minimal impact on churn
- Customers without a partner churn more


## Getting Started

### Prerequisites

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### Installation

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

### Usage

1. Clone or download this repository
2. Ensure the CSV file is in the correct path
3. Open `Telecom_Churn.ipynb` in Jupyter Notebook or VS Code
4. Run the cells sequentially to perform the analysis



