🩺 Diabetes Prediction Model – First MLOps Project (FastAPI + Docker + K8s)
This project helps you learn **Building and Deploying an ML Model** using a simple and real-world use case: predicting whether a person is diabetic based on health metrics. We’ll go from:
- ✅ Model Training
- ✅ Building the Model locally
- ✅ API Deployment with FastAPI
- ✅ Dockerization
- ✅ Kubernetes Deployment
---
## 📊 Problem Statement
Predict if a person is diabetic based on:
- Pregnancies
- Glucose
- Blood Pressure
- BMI
- Age
We use a Random Forest Classifier trained on the **Pima Indians Diabetes Dataset**.
---
## 🚀 Quick Start
### 1. Clone the Repo
```bash
git clone https://github.com/iam-veeramalla/first-mlops-project.git
cd first-mlops-project
```
### 2. Create Virtual Environment
```
python3 -m venv .mlops
source .mlops/bin/activate
```
### 3. Install Dependencies
```
pip install -r requirements.txt
```
## Train the Model
```
python train.py
```
## Run the API Locally
```
uvicorn main:app --reload
```
### Sample Input for /predict
```
{
  "Pregnancies": 2,
  "Glucose": 130,
  "BloodPressure": 70,
  "BMI": 28.5,
  "Age": 45
}
```
## Dockerize the API
### Build the Docker Image
```
docker build -t diabetes-prediction-model .
```
### Run the Container
```
docker run -p 8000:8000 diabetes-prediction-model
```
## Deploy to Kubernetes
```
kubectl apply -f diabetes-prediction-model-deployment.yaml
```
---
## 🙌 Reference
 [GitHub](https://github.com/iam-veeramalla).
---
## 📢 License
Apache 2.0
---
## What this project helps me understand
This project is designed as a compact, hands-on MLOps primer. Working through it will help you understand:
- End-to-end MLOps workflow: from data to deployed model.
- Data handling basics: loading a CSV dataset and preparing features for modeling.
- Model development: training, evaluating, and persisting a Random Forest model.
- Reproducibility: using virtual environments and requirements to pin dependencies.
- Serving models: building a production-like REST API with FastAPI and Uvicorn.
- Containerization: writing a Dockerfile, building images, and running containers.
- Orchestration: deploying applications to Kubernetes with manifests and port-forwarding.
- Local cluster tooling: using kind/minikube for testing deployments locally.
- Deployment concerns: model versioning, API contract (OpenAPI/Swagger), and simple scaling considerations.
- Practical DevOps skills: CLI usage (git, docker, kubectl), basic debugging, and verifying pod/service status.
Working through these steps gives practical intuition about how ML projects move from notebooks to reliable, deployable services.
---
*All steps and configuration are included so anyone can reproduce and deploy the project from scratch.*