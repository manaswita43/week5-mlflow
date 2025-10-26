# 🧠 MLflow Integration in MLOps Pipeline

This project demonstrates how to **integrate MLflow** into an existing MLOps pipeline for experiment tracking, model versioning, and evaluation — replacing traditional model tracking using DVC.  
We use the **Iris dataset** and train multiple Random Forest models to log parameters, metrics, and models into the **MLflow Tracking Server** and **Model Registry**.

---

## Overview

In this assignment, we:
- Introduce **hyperparameter tuning** into the training loop.
- **Log experiments** (parameters, metrics, and models) using MLflow.
- **Compare experiments visually** using MLflow’s metric visualization interface.
- **Remove DVC model tracking** and replace it with MLflow Model Registry.
- **Fetch the best/latest model** from the MLflow Model Registry for evaluation.

---

## Objective

By the end of this tutorial, you will be able to:
- Set up an **MLflow Tracking Server**.
- Log experiment parameters, evaluation metrics, and trained models.
- Use the **MLflow UI** to compare and select the best experiment.
- Register and manage models using the **MLflow Model Registry**.

---

## Environment Details

**Python version:** 3.10  
**Key Libraries:**  
- `mlflow`
- `pandas`
- `scikit-learn`
- `joblib`

---

## Setup Instructions

### 1. Start a screen
```bash
screen -S mlflow-week5
```

### 2. Install necessary libraries
```bash
pip install mlflow scikit-learn joblib pandas
```

### 3. Run mlflow as a server
```bash
mlflow server --host 0.0.0.0 --port 8100 --allowed-hosts '*' --cors-allowed-origins '*'
```
If running on Google Cloud Workbench, ensure:
- Firewall allows ingress on port 8100
- The MLflow UI can be accessed via:
```cpp
http://<external-ip>:8100
```

## Steps Performed

- Connect to MLflow Tracking Server
- Remove DVC Model Tracking
- Load and Split Dataset
- Train and Log Experiments
- Visualize and Compare in MLflow UI
- Register the Best Model
- Fetch and Evaluate the Best Model

## Key Learnings
- How to log, track, and visualize ML experiments with MLflow.
- How to use the Model Registry for version control and deployment.
- How to replace traditional DVC-based model management with MLflow.

## Project Structure
```
mlflow-assignment/
│
├── data/
│   └── iris.csv
│
├── notebooks/
│   └── mlflow_integration.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```
