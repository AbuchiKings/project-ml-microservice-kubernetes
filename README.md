[![CircleCI](https://dl.circleci.com/status-badge/img/gh/AbuchiKings/project-ml-microservice-kubernetes/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/AbuchiKings/project-ml-microservice-kubernetes/tree/main)


#### Project Overview

This contains a Machine Learning Microservice, built on **Scikit-Learn**. It contains a model that predicts house prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). 

## What does this project do?

- Run docker container
- Upload container into a public registry (hub.docker.com)
- Run the deployed application in a Kubernetes cluster
- Integrate with CircleCI for continuous integration

## Requirements
 - Python 3.7

## Steps

### Step 0
- Clone repo to local machine

### Step 1: Install dependencies
- Set up the environment by running `make setup`. This will create a virtual environment in your home directory called `.devops`
- Install dependencies by running `make install`
- (Optionally) Lint application (requires hadolint)

### Step 2: Run Docker container
- Run application with command `./run_docker.sh`

### Step 3: Upload to Docker Hub
- In  `./upload_docker.sh` file, edit variable dockerpath (line 8) and change the docker username to a personalized one.
- To upload to docker hub, run `./upload_docker.sh`

### Step 4: Kubernetes deployment
- To deploy to kubernetes, run `./run_kubernetes.sh`