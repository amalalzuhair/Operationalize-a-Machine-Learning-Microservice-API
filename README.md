[![amalalzuhair](https://circleci.com/gh/amalalzuhair/Operationalize-a-Machine-Learning-Microservice-API.svg?style=svg)](https://app.circleci.com/pipelines/github/amalalzuhair/Operationalize-a-Machine-Learning-Microservice-API)

## Project Overview

In this project I have used a pre-trained `sklearn` model that has been trained to predict housing prices in Boston according to several features. I used docker technology to containerize the application. And I used Kubernetes technology as a cluster provider for my containerized application. This project is in collaboration with Udacity nanodegree for Cloud DevOps Engineer program. 

## Project Motivation: 
To practice operationizing Machine learning models using Docker, Kubernetes and other technologies taught in the "Microservices at scale, using AWS and Kubernetes" Course in Udacity nanodegree for Cloud DevOps Engineer program.

### Tech Stack: 
* Python
* Flask
* Kubernetes
* Docker
* Pylint
* Hadolint
* CircleCI

# Setup the Environment:

1. Create a virtualenv with Python 3.7 and activate it:
```bash
python3 -m pip install --user virtualenv
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
2. Run `make install` to install the necessary dependencies

3. Run `make lint` to check for linting errors

# Run in Docker container
* Make sure you install docker following these instructions: https://docs.docker.com/get-docker/
1. Run docker container `./run_docker.sh`
2. Make predicition using `./make_prediction.sh`
3. Upload to docker hub `./upload_docker.sh`

# Run in Kubernetes Cluster

1. Install minikube and virtualbox
2. run `minikube start` to start a local cluster 
3. Run `./run_kubernetes.sh` to start the kubernetes pod and create the flask app in the container.
4. Run `./make_prediction.sh` to make predictions


## Files Structure: 
* App.py: Python application file that contains a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. 
* Dockerfile used to support in the steps for building the docker image 
* make_prediction.sh used to test the ML model by passing the data needed to be validated and adding the output into docker_output.txt and kubernetes_out.txt 
* Makefile is used to facilitate all the needed commands for make logic. 
* requirements.txt has all the needed libraries and dependencies. 
* run_docker.sh used to run docker container
* upload_docker.sh used to upload to docker hub 
* run_kubernetes.sh used to deploy in Kubernetes 