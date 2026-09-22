# Student Final Grade Prediction using ANN

A machine learning project that uses an **Artificial Neural Network (ANN)** to predict a student's final mathematics grade (`G3`) based on demographic, academic, social, and behavioral attributes from the **UCI Student Performance Dataset**.

## Overview

The project follows an end-to-end regression pipeline:

* Exploratory Data Analysis (EDA)
* Correlation analysis
* Categorical feature encoding
* Train-test splitting
* Feature standardization
* ANN model development using TensorFlow/Keras
* Model training with Early Stopping
* Performance evaluation
* Sample grade prediction

## Model Architecture

The ANN consists of:

* Input layer
* Dense layer — 64 neurons, ReLU
* Dropout — 20%
* Dense layer — 32 neurons, ReLU
* Dropout — 20%
* Dense layer — 16 neurons, ReLU
* Output layer — 1 neuron

**Optimizer:** Adam
**Loss:** Mean Squared Error (MSE)
**Batch Size:** 16
**Maximum Epochs:** 200
**Early Stopping:** Enabled

## Results

The model achieved the following performance on the test set:

| Metric   |      Score |
| -------- | ---------: |
| MAE      | **1.7753** |
| MSE      | **5.9061** |
| RMSE     | **2.4302** |
| R² Score | **0.7120** |

The model explains approximately **71.2% of the variation** in final mathematics grades in the test dataset.

## Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow / Keras
* Jupyter Notebook

## Project Structure

```text
Student-Performance-ANN/
│
├── data/
│   └── student-mat.csv
│
├── model/
│   └── student_ann.keras
│
├── results/
│   ├── correlation_matrix.png
│   ├── loss_curve.png
│   └── actual_vs_predicted.png
│
├── student_performance_ann.ipynb
└── README.md
```

## Dataset

The project uses the **Student Performance Dataset** from the UCI Machine Learning Repository.

The target variable is:

* `G3` — Final mathematics grade

Previous grades (`G1` and `G2`) are also included as input features.