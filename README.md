# Kubernetes Deployment and Scaling Demo

## Project Overview

This project demonstrates how to deploy a containerized application on Kubernetes and manage application scaling using deployments and replicas.

The application is containerized using Docker and deployed on a local Kubernetes cluster created using Minikube.

## Technologies Used

* Kubernetes
* Docker
* Minikube
* Node.js
* kubectl

## Project Structure

k8s-scaling-demo
│
├── app.js
├── package.json
├── Dockerfile
├── deployment.yaml
├── service.yaml
└── README.md

## Deployment Steps

Start Minikube

```
minikube start
```

Use Minikube Docker environment

```
eval $(minikube docker-env)
```

Build Docker image


docker build -t k8s-demo .


Deploy application to Kubernetes


kubectl apply -f deployment.yaml


Check running pods


kubectl get pods


Scale the deployment


kubectl scale deployment demo-deployment --replicas=5


Verify scaling


kubectl get pods


## Key Kubernetes Concepts Demonstrated

* Pods
* Deployments
* ReplicaSets
* Containerized Applications
* Manual Scaling

## Learning Outcome

Through this project I learned:

* How containerized applications are deployed in Kubernetes
* How Kubernetes manages replicas using deployments
* How scaling works in Kubernetes clusters

## Author

Shravani Gulhane
