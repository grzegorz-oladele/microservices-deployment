# microservices-deployment

Kubernetes project tasked with deploying and updating the application https://github.com/grzegorz-oladele/microservcies-training
on test and production environment.

## Requirements
### 1. Run Docker Desktop application
### 2. Check if you create a kubernetes cluster on your local machine by Docker
![](images/docker-1.jpeg)
![](images/docker-2.jpg)
![](images/docker-3.jpg)

# How to deploy application?
**command**: `kubectl apply -f k8s` -> if you need deploy an application on your local kubernetes cluster

*Any changes regarding project configuration should be made in .yml files in k8s directory
#### HERE WE GO!
Now you can test application on your local kubernetes cluster on http://localhost:8100/api/** \
Full microservices-deployment documentation you can find in project repo -> https://github.com/grzegorz-oladele/microservcies-training