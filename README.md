# Big Data Analytics Final Project - MLOps-end-to-end-project - IBA Sp. 2023

Group Members: Bilal Naseem, M. Salman Malik, Jahanzaib Faisal

End-to-end prediction model development using PySpark with Docker and Streamlit

Project Demo Video: https://www.youtube.com/watch?v=M-w6dpkdUFs

# Use Case

Development and deployment of a Random Forest Classifier using Spark ML to determine loan approval success based on individual profile and default status

* Exploratory data analysis using PySpark
* Feature engineering using Spark SQL
* Model developement using Spark ML and Vector Assembler to create ML pipelines
* Compiled models in separate pickle files to migrate from development to staging environment
* Developed UI using Streamlit 
* Build Docker Image to containerise model development
* Establish API connect using Postman 
* A network between the two Docker containers—one for PySpark flask and the second one for the streamlit UI
* Includes a CI/CD pipeline configured through GitHub Actions
* Automating the process of building and deploying the Docker images for both the PySpark API and the Streamlit API, as soon as new commits are pushed onto the main branch

# Docker Images

Docker images are hosted on Docker Hub. Here is the command structure to pull an image:

```shell
docker pull bilal326/bda-final-project-streamlitapi:latest
```

```shell
docker pull bilal326/bda-final-project-pysparkapi:latest
```

# Quick start

By default docker-compose uses images defined in the file with `latest` tag.

```shell
docker-compose up -d
```

# Development

When in development mode use below command to build the image to get quick feedback loop for fixes / new features.

This will build docker image from local build context

```shell
docker-compose up -d --build
```

# Accessing the Application UI

To interact with the application user interface, open a web browser and navigate to the following address: 

http://localhost:8501/

This will open the application's UI on your local machine, allowing you to interact directly with the application.
You can go ahead and input the values for the features and click Get Predictions to get results.
