# Operationalizing Machine Learning

This project consists of two phases :  using Azure to configure a cloud-based machine learning production model, deploy it, and consume it. This part is mainly done by using the Azure ML studio and the Terminal (GitBash). The second phase involves creating, publishing, and consuming a pipeline using the Python SDK and Jupyter Notebook. In both phases we work with the [Bank Marketing dataset](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv). The goal is to predict whether bank customers subscribe to term deposits (target variable `y`=1) or not (target variable `y`=0) based on the values of input variables (age, job, marital, education, etc).

The main steps followed in the project are :

1. Authentication
2. Automated ML Experiment
3. Deploy the best model
4. Enable logging
5. Swagger Documentation
6. Consume model endpoints
7. Create and publish a pipeline
8. Documentation

We can skip the authentication step since we are not authorized to create a security principal because we are using the lab Udacity provided to us.

## Architectural Diagram

![Architectural Diagram](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/architectual_diagram.png) 

## Key Steps

### Step 1 : Authentication

As mentioned before, the autentication step was done for us. In this step, we need to install the Azure Machine Learning Extension which allows us to interact with Azure ML Studio, part of the `az` command and create a `Service Principal account`. 

### Step 2 : Automated ML Experiment

In this step, we created an experiment using Automated ML, configured a compute cluster, and used that cluster to run the experiment. 

#### 2.1 : Registered Datasets

Below, a screenshot of 'Registered Datasets" in ML Studio showing that Bankmarketing dataset is available.

![Architectural Diagram](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/01_registered_datasets.PNG) 

#### 2.2 : Experiment Completed

The experiment is shown as completed.

![Architectural Diagram](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/02_autoML_experiment.PNG) 

### Step 3 : Deploy the Best Model

### Step 4 : Enable logging

### Step 5 : Swagger Documentation

### Step 6 : Consume model endpoints

### Step 7 : Create and publish a pipeline

### Step 8 : Documentation

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
