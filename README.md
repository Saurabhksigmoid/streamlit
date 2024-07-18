# Streamlit Kubernetes Project

This project demonstrates how to develop, containerize, and deploy a Streamlit application using Docker and Kubernetes.

## Project Structure

streamlit-k8s/
├── app.py
├── Dockerfile
├── requirements.txt
├── kubernetes/
│ ├── deployment.yaml
│ ├── service.yaml
├── .github/
│ └── workflows/
│ └── deploy.yml
├── README.md


## Getting Started

### Prerequisites

- Docker
- Kubernetes (Minikube or a managed Kubernetes service)
- kubectl
- GitHub account

### Running Locally

```bash
pip install -r requirements.txt
streamlit run app.py

### Building Docker Image

docker build -t streamlit-app .
docker run -p 8501:8501 streamlit-app

### Deploying to Kubernetes

kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
minikube service streamlit-service

