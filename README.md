# End-to-End Text Summarizer Project
This repository contains an end-to-end implementation of a text summarization project, showcasing the entire pipeline from setup to deployment on AWS. The project is designed to provide a comprehensive understanding of building and deploying a machine learning model with proper software engineering practices.

![text](https://github.com/ganeshmore99/Text-Summarization-NLP-Project/assets/85934803/37ca2597-1f30-4147-9d61-3da758742c30)


## Table of Contents
#### Introduction
#### Repository Setup
#### Project Template Creation
#### Project Setup and Requirements Installation
#### Logging, Utils, and Exceptions Modules
#### Components Modular Code Implementation
#### Training Pipeline
#### MLOps Tools Implementation
#### Prediction Pipeline and User App Creation
#### Docker
#### GitHub Actions
#### CI/CD Deployment on AWS Cloud

## Introduction
This project aims to create a text summarizer using modern machine learning techniques. The summarizer takes a block of text as input and produces a concise summary. The entire pipeline, from data preprocessing to model deployment, is covered.

## Repository Setup
Initialize a new GitHub repository.
Clone the repository to your local machine.
Set up a basic directory structure for the project.

## Project Template Creation
Create a project template with necessary directories and files.
Ensure the template supports modular code development.

## Project Setup and Requirements Installation
Create a virtual environment.
Install all necessary dependencies from requirements.txt.

```
pip install -r requirements.txt
```
## Logging, Utils, and Exceptions Modules
Set up logging to track the project's progress and issues.
Create utility functions to avoid code redundancy.
Implement custom exception handling for better error management.

## Components Modular Code Implementation
Develop modular code for different components of the project:
1. Data Ingestion
2. Data Validation
3. Data Transformation
4. Model Training
5. Model Evaluation

## Training Pipeline
Implement the training pipeline to train the text summarizer model.
Save the trained model for later use.

## MLOps Tools Implementation
Integrate MLOps tools to automate and monitor the ML pipeline.
Use tools like MLflow, DVC, or other relevant MLOps frameworks.

## Prediction Pipeline and User App Creation
Create a prediction pipeline to use the trained model for inference.
Develop a simple web app to allow users to interact with the model and get text summaries.

## Docker
Create a Dockerfile to containerize the application.
Build and test the Docker image locally.

## GitHub Actions
Set up GitHub Actions for CI/CD.
Create workflows to automate testing, building, and deployment processes.

## CI/CD Deployment on AWS Cloud
Configure AWS services for deployment (e.g., EC2, S3, RDS).
Deploy the application using CI/CD pipelines set up with GitHub Actions.

## Workflows

1. Update config.yaml
2. Update params.yaml
3. Update entity
4. Update the configuration manager in src config
5. update the conponents
6. update the pipeline
7. update the main.py
8. update the app.py


# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/ganeshmore99/Text-Summarization-NLP-Project.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n textS python=3.8 -y
```

```bash
conda activate textS
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```


```bash
Author: Ganesh More
Email: ganeshmore5199@gmail.com

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/text-s

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app


## Conclusion
This project demonstrates a complete pipeline for building, training, and deploying a text summarization model using machine learning and modern software engineering practices. The use of MLOps tools and CI/CD pipelines ensures a robust and scalable solution.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
