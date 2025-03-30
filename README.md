# **Steps For End to End diabetes_prediction Process**
## Architecture Diagram 

![image](https://github.com/user-attachments/assets/eaae1f0e-52e4-4e99-b481-fe5cc9072137)

## Docker 


### FROM python: slim-bullseye  # start with lightweight python environment. ###
### COPY . . /src              # copy your currect files to a directory name "src" in the image. ###
### WORKDIR /src                # set the working directory inside the image to "src". ###
### Run pip install -r requirenments.txt # install python dependencies. ###
### ENTRYPOIN ["python","app.py"] # run "app.py" when the container starts. ###
### EXPOSE 8000 # prepare to listen on port 8000 ###




## CICD  Pipeline (GitHub Actions) ##

**Triggered on push to main, excluding README.md.**

**Two jobs: integration and build-push-package**.

### 1. Intregation: ###
**Matrix: Python 3.9, 3.10, 3.11**.

**Setup Python, install deps**.

**Lint code using ruff**.

### 2. Build and Push Package: ###

**Depends on integration**.

**Build Docker image and push to Docker Hub**.



## Step 1 -> Install required Libraries.
Step 2 -> Import required packages.
Step 3 -> Load data.
Step 4 -> Data understanding.
Step 5 -> Exploratory Data Analysis.
Step 6 -> Feature Engineering.
Step 7 -> Data pre-processing.
Step 8 -> Modelling.
Step 9 -> Model Evaluation.
Step 10 -> Hyper-parameter tuning and Re-modelling.
Step 11 -> Extract Model.
Step 12 -> Model Deployment.
Step 13 -> Integrate a Machine Learning deployed model in external application
Step 14 -> mlops(github, docker image and containerization, ci/cd, aws ec2 )
