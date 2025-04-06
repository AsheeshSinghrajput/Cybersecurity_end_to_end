# **Steps For End to End Cybersecurity Process**
📘 [Click here to view the notebook with all steps and outputs](https://github.com/AsheeshSinghrajput/Cybersecurity_end_to_end/blob/main/NSL-KDD-Cybersecurity.ipynb) 

## Architecture Diagram 

![image](https://github.com/user-attachments/assets/eaae1f0e-52e4-4e99-b481-fe5cc9072137)

## Docker 


 **FROM python: slim-bullseye  # start with lightweight python environment.**

**COPY . . /src              # copy your currect files to a directory name "src" in the image.**

**WORKDIR /src                # set the working directory inside the image to "src".**

**Run pip install -r requirenments.txt # install python dependencies.**

**ENTRYPOIN ["python","app.py"] # run "app.py" when the container starts.**

**EXPOSE 8000 # prepare to listen on port 8000**


## CICD  Pipeline (GitHub Actions) ##

### This project uses GitHub Actions for Continuous Integration (CI) and Continuous Deployment (CD).

**Triggered on push to main, excluding README.md.**

**Two jobs: integration and build-push-package**.

### 1. Intregation: ###
**Matrix: Python 3.9, 3.10, 3.11**.

**Setup Python, install dependencies.**.

**Lint code using ruff**.

### 2. Build and Push Package: ###

**Depends on integration**.

**Build Docker image and push to Docker Hub**.
