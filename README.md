[![nassimatoumi](https://circleci.com/gh/nassimatoumi/project-ml-microservices-kubernetes.svg?style=svg)](https://circleci.com/gh/nassimatoumi/project-ml-microservices-kubernetes)

## Project Overview

In this project, a containerized app uses a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This app serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.
You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

### Main file description
`app.py`: Contains the application code
`model_data/`: This directory contains the pre-trained model that is used by the application.
`Dockerfile`: Contains the commands that configure the Docker image.
`run_docker.sh`: Contains the commands that build the Docker image and run the application on Docker.
`docker_out.txt`: Contains the log output from performing a prediction using Docker.
`upload_docker.sh`: Contains the commands that upload the Docker image to the user's repository.
`run_kubernetes.sh`: Contains the commands tha run the application on Kubernetes using the previously uploaded Docker image.
`kubernetes_out.txt`: Contains the log output from performing a prediction using Kubernetes.


---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Making predictions
Once the app is running, open a new terminal window and run: `./make_prediction.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
