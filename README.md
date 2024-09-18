# MLOps

# Customer Satisfaction Prediction Pipeline

This repository demonstrates how ZenML can be used to build a production-ready pipeline for predicting customer satisfaction scores using the Brazilian E-Commerce Public Dataset by Olist. The dataset contains 100,000 orders from 2016-2018 with features such as order status, price, payment, freight performance, customer location, product attributes, and reviews.

## Objective
Predict customer satisfaction scores for future purchases using features like order status, price, and payment information. The pipeline ensures real-time prediction capabilities with end-to-end automation for training, deploying, and tracking models.

## Key Features
- **ZenML-powered ML pipeline**: Automates model training, deployment, and tracking, integrating seamlessly with tools like MLflow for experiment tracking and deployment.
- **MLflow integration**: Tracks metrics, model parameters, and automates model deployment based on performance thresholds.
- **Streamlit Application**: A demo app utilizing the latest deployed model to predict customer satisfaction scores based on input data.

## Steps in the Pipeline
### 1. Training Pipeline:
- `ingest_data`: Ingests data and creates a DataFrame.
- `clean_data`: Cleans the data and removes unwanted columns.
- `train_model`: Trains the model and logs it with MLflow.
- `evaluation`: Evaluates the model and logs metrics with MLflow.

### 2. Deployment Pipeline:
- Extends the training pipeline by adding:
  - `deployment_trigger`: Checks if the model meets deployment criteria based on MSE.
  - `model_deployer`: Deploys the model as a service using MLflow.

## How to Run
### Clone the repository and install dependencies:
```bash
git clone https://github.com/zenml-io/zenml-projects.git
cd zenml-projects/customer-satisfaction
pip install -r requirements.txt
