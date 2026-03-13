# Kubernetes Deployment and Scaling Demo

## Project Overview

This project demonstrates how to deploy a containerized application on Kubernetes and manage application scaling using deployments and replicas.

The application is containerized using Docker and deployed on a local Kubernetes cluster created using Minikube.

---

## Technologies Used

* Kubernetes
* Docker
* Minikube
* Node.js
* kubectl

---

## Project Structure

```
k8s-scaling-demo
│
├── app.js
├── package.json
├── Dockerfile
├── deployment.yaml
├── service.yaml
└── README.md
```

---

## Start Minikube Cluster

```bash
minikube start
```

---

## Use Minikube Docker Environment

```bash
eval $(minikube docker-env)
```

This allows Docker images to be built directly inside the Minikube environment.

---

## Build Docker Image

```bash
docker build -t k8s-demo .
```

---

## Deploy Application to Kubernetes

```bash
kubectl apply -f deployment.yaml
```

---

## Verify Running Pods

```bash
kubectl get pods
```

---

## Scale the Deployment

Increase the number of pods to handle higher load.

```bash
kubectl scale deployment demo-deployment --replicas=5
```

---

## Verify Scaling

```bash
kubectl get pods
```

You should see multiple running pods created by the deployment.

---

## Monitor Pod Resource Usage

```bash
kubectl top pods
```

This command shows CPU and memory usage of running pods.

---

## Key Kubernetes Concepts Demonstrated

* Pods
* Deployments
* ReplicaSets
* Containerized Applications
* Manual Scaling
* Resource Monitoring

---

## Learning Outcome

Through this project I learned:

* How containerized applications are deployed in Kubernetes
* How Kubernetes manages replicas using deployments
* How scaling works in Kubernetes clusters
* How resource metrics can be monitored

---

## Author

Shravani Gulhane
