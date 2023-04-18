# microservices-deployment

Kubernetes project tasked with deploying and updating the application https://github.com/grzegorz-oladele/microservcies-training
on test and production environment.

## Requirements
### 1. Run Docker Desktop application
### 2. Check if you create a kubernetes cluster on your local machine by Docker
![](images/docker-1.jpeg)
![](images/docker-2.jpg)
![](images/docker-3.jpg)
### 3. Check if you have helm on your local machine
**command**: `helm version`\
if you don't have helm on your local machine follow to instruction -> https://helm.sh/docs/intro/install/
# How to deploy application?
1. In dev environment \
   a. **command**: `kubectl create namespace dev` -> create dev namespace \
   b. **command** -> `helm install dev-release microservices-deployment/ --values microservices-deployment/values.yml -f microservices-deployment/values-dev.yml -n dev` -> if you need deploy an application to kubernetes cluster on dev namespace\
   c. **command**: `helm upgrade dev-release microservices-deployment/ --values microservices-deployment/values.yml -f microservices-deployment/values-dev.yml -n dev` -> if you need update your kubernetes cluster on dev namespace


2. In test environment \
   a. **command**: `kubectl create namespace test` -> create test namespace \
   b. **command**: `helm install test-release microservices-deployment/ --values microservices-deployment/values.yml -f microservices-deployment/values-test.yml -n test` -> if you need deploy an application to kubernetes cluster on test namespace\
   c. **command**: `helm upgrade test-release microservices-deployment/ --values microservices-deployment/values.yml -f microservices-deployment/values-test.yml -n dev` ->  if you need u[date your kubernetes cluster in test namespace

*Any changes regarding project configuration should be made in main values.yml file or in namespace-specific files

#### HERE WE GO!
Now you can test application on your local kubernetes cluster on http://localhost:8100/api/** \
Full microservices-deployment documentation you can find in project repo -> https://github.com/grzegorz-oladele/microservcies-training