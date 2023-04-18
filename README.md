# microservices-deployment

Kubernetes project tasked with deploying and updating the application https://github.com/grzegorz-oladele/microservcies-training
on test and production environment.

## Requirements
### 1. Access to Kubernetes Cluster
command: kubectl version - check if you have Kubernetes installed on your local machine
command: helm version - check if you have Helm installed on your local machine
### 2a. Run Docker Desktop application
### 2b. Check if you create a kubernetes cluster on your local machine by Docker
![](images/docker-1.jpeg)
![](images/docker-2.jpg)
![](images/docker-3.jpg)

How deploy application?
1. In dev environment
a. create dev namespace ->  kubectl create namespace dev
b. use command -> helm install dev-release microservices-deployment/ --values microservices-deployment/values.yml -f microservices-deployment/values-dev.yml -n dev
c. use command if you need update your kubernetes cluster -> helm uprade
2. 

2. In test environment
a. create dev namespace kubectl create namespace test
b. use command helm install test-release microservices-deployment/ --values microservices-deployment/values.yml -f microservices-deployment/values-test.yml -n test

*Any changes regarding project configuration should be made in values*.yml files

HERE WE GO!
Now you can test application in your local kubernetes cluster on http://localhost:8100/api/**
Full microservices-deployment documentation you can find in project repo -> https://github.com/grzegorz-oladele/microservcies-training
