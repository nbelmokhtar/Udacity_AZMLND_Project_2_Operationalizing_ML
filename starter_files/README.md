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

Below, a screenshot of `Registered Datasets` in ML Studio showing that `Bank-marketing` dataset is available.

![Registered Datasets](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/01_registered_datasets.PNG) 

#### 2.2 : Experiment Completed

The experiment `Bank-Marketing-AutoML-Exp` is shown as completed.

![AutoML Experiment](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/02_autoML_experiment.PNG) 

#### 2.3 : Best Model

The Screenshot below shows the best model after the experiement completes.`Voting Ensemble` achieved an accuracy of 91.80%.

![Best Model](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/04_autoML_best_model.PNG)  

### Step 3 : Deploy the Best Model

Deploying the Best Model using the `Azure Container Instance` and `Enable authentication` will allow to interact with the HTTP API service and interact with the model by sending data over POST requests.

![Best Model Deploy](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/05_autoML_best_model_deploy.PNG)

The deploy status shows succeeded.

![Best Model Deploy Status](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/06_autoML_best_model_deploy_status.PNG)

### Step 4 : Enable logging

![Logs Py File](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/07_logs_py.PNG)

![Run Logs Py File](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/08_run_logs_py.PNG)

![App Insights Enabled](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/09_app_insights_enabled.PNG)

### Step 5 : Swagger Documentation

![Run Swagger](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/10_run_swagger_sh.PNG)

![Local Host](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/12_local_host_8000_explore.PNG)
![Local Host](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/13_local_host_8000_explore.PNG)
![Local Host](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/14_local_host_8000_explore.PNG)
![Local Host](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/15_local_host_8000_explore.PNG)
![Local Host](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/16_local_host_8000_explore.PNG)

### Step 6 : Consume model endpoints

![Endpoint](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/17_endpoint_py.PNG)

![Run Endpoint](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/18_run_endpoint_py_1.PNG)

![Benchmark](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/19_benchmark_sh.PNG)

![Run Benchmark](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/20_run_benchmark_sh_1.PNG)

### Step 7 : Create, Publish and Consume a Pipeline

The pipeline section of Azure ML Studio shows that the pipeline has been created and it's running.

![Create a Pipeline](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/21_pipeline_created.PNG)

![Pipeline Running](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/22_pipeline_running.PNG)

![Pipeline Running](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/23_pipeline_running.PNG)

![Pipeline Completed](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/24_pipeline_completed.PNG)

![Pipelines Completed](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/25_pipelines_completed.PNG)

The pipeline section of Azure ML Studio shows that the pipeline endpoint.

![Pipeline Endpoints](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/26_pipeline_endpoints.PNG)

The Bankmarketing dataset with the AutoML module.

![Pipeline Dataset and Automl](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/27_pipeline_dataset_and_automl_module.PNG)

The `Published pipeline overview` shows a REST endpoint and a status of ACTIVE.

![Published Pipeline](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/28_published_pipeline_overview.PNG)

`Use RunDetails Widget` shows the step runs.

![RunDetails](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/29_rundetails.PNG)

Scheduled run

![Scheduled Run](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/30_scheduled_runs_1.PNG)

![Scheduled Run](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/30_scheduled_runs_2.PNG)

![Scheduled Run](https://github.com/nbelmokhtar/Udacity_AZMLND_Project_2_Operationalizing_ML/blob/master/starter_files/screenshots/31_automl_module.PNG)



### Step 8 : Documentation

## Screen Recording

Here's a [screencast](https://www.dropbox.com/s/9f96vbuqten905g/NB-Udacity-AZMLND-Project-2.mp4?dl=0) recording that shows the entire process of the working ML application.

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
