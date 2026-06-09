# Medical Insurance Cost Prediction on AWS SageMaker

## Overview

This project develops and evaluates machine learning models to predict individual medical insurance costs using demographic and lifestyle information. The solution is implemented in **AWS SageMaker** and compares traditional regression techniques with SageMaker-native machine learning algorithms and neural networks.

The objective is to estimate insurance charges based on factors such as age, BMI, smoking status, number of dependents, gender, and geographic region.

---

## Problem Statement

Healthcare costs vary significantly across individuals due to a combination of demographic, behavioral, and geographic factors. Accurate cost prediction can help:

- Insurance providers improve pricing strategies
- Healthcare organizations forecast expenditures
- Individuals better understand factors influencing insurance premiums

This project builds predictive models that estimate medical insurance charges from customer characteristics.

---

## Dataset

The dataset contains information about insurance beneficiaries in the United States.

### Features

| Feature | Description |
|----------|-------------|
| age | Age of the primary beneficiary |
| sex | Gender of the insurance contractor |
| bmi | Body Mass Index |
| children | Number of dependents covered by insurance |
| smoker | Smoking status |
| region | Residential region in the United States |
| charges | Medical insurance cost (target variable) |

### Target Variable

- **charges**: Individual medical insurance expenses billed by the insurer.

---

## Project Workflow

### 1. Data Exploration and Analysis

Performed exploratory data analysis (EDA) to:

- Inspect dataset structure
- Identify missing values
- Analyze feature distributions
- Examine relationships between variables
- Calculate summary statistics
- Generate correlation analysis

Visualizations include:

- Histograms
- Distribution plots
- Pair plots
- Correlation heatmaps
- Regression plots

---

### 2. Data Preprocessing

Preprocessing steps include:

- Converting categorical variables into numerical representations
- Feature engineering and transformation
- Train-test split
- Preparing data for SageMaker training jobs

---

### 3. Baseline Model: Linear Regression

A traditional Scikit-Learn Linear Regression model is trained as a baseline.

Evaluation metrics include:

- Mean Absolute Error (MAE)
- R² Score
- Adjusted R² Score

---

### 4. AWS SageMaker Linear Learner

The project uses the SageMaker built-in **Linear Learner** algorithm to:

- Train a scalable regression model
- Experiment with hyperparameters
- Compare performance against Scikit-Learn Linear Regression

Benefits include:

- Managed training infrastructure
- Efficient model deployment
- Hyperparameter customization

---

### 5. Neural Network Regression Model

A more advanced Artificial Neural Network (ANN) model is developed to capture non-linear relationships within the data.

Experiments include:

- Multiple hidden layers
- Different neuron configurations
- Regularization techniques
- Dropout tuning

---

### 6. Model Deployment

The trained SageMaker model is deployed as an endpoint for real-time inference.

The deployment pipeline demonstrates:

- Model hosting in SageMaker
- Endpoint creation
- Prediction requests
- Real-time cost estimation

---

## Technologies Used

- Python
- AWS SageMaker
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- TensorFlow / Keras
- Jupyter Notebook

---

## Project Structure

```text
medical-insurance-cost-prediction/
│
├── medical_insurance_prediction_notebook.ipynb
├── insurance.csv
├── README.md
│
├── data/
│   └── insurance.csv
│
├── models/
│   ├── linear_regression/
│   ├── linear_learner/
│   └── neural_network/
│
└── images/
    ├── correlation_heatmap.png
    ├── distribution_plots.png
    └── model_results.png

