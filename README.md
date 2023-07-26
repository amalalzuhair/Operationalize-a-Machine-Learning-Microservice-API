[![amalalzuhair](https://circleci.com/gh/amalalzuhair/Operationalize-a-Machine-Learning-Microservice-API.svg?style=svg)](https://app.circleci.com/pipelines/github/amalalzuhair/Operationalize-a-Machine-Learning-Microservice-API)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### How to run the project

* 1. Setup the Environment:

* Create a virtualenv with Python 3.7 and activate it:
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* 2. Run `make install` to install the necessary dependencies

* 3. Run docker container `./run_docker.sh`

* 4. Upload to docker hub `./upload_docker.sh`

* 5. Deploy in Kubernetes  `./run_kubernetes.sh`

## Files Structure: 
* App.py: Python application file that contains a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. 
* Dockerfile used to support in the steps for building the docker image 
* make_prediction.sh used to test the ML model by passing the data needed to be validated and adding the output into docker_output.txt and kubernetes_out.txt 
* Makefile is used to facilitate all the needed commands for make logic. 
* requirements.txt has all the needed libraries and dependencies. 
* run_docker.sh used to run docker container
* upload_docker.sh used to upload to docker hub 
* run_kubernetes.sh used to deploy in Kubernetes 