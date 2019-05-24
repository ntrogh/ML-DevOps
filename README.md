# Managing your data science pipeline (Techorama 2019)

This repo contains the sample code for my session at Techorama 2019.

## Step 1: introducing the ML model and Diabetes dataset

We're using a Ridge Regression classical machine learning model for demonstration purposes. If you use a different ML model, make sure to add the corresponding conda dependencies in step 3.

[Ridge Regression on the Diabetes dataset](./00-diabetes-regression.ipynb)

## Step 2: configuring the Azure ML workspace

In this step we're configuring the Azure Machine Learning service workspace, which will be used in the next step. It will connect to an existing workspace or create a new one if none can be found.

This notebook will generate the .azureml/config.json file on disk.

[Configuring the Azure ML workspace](./01-aml-configuration.ipynb)

## Step 3: integrating Azure ML using the Python SDK

In this step we're modifying the base ML model code to integrate with the Azure Machine Learning service.
First it creates an experiment and corresponding run to track the execution of the ML model. Next, it goes through the steps of deploying the ML model as a web service to Azure Container Instance.

[Integrating the model with Azure ML](./02-diabetes-with-aml.ipynb)


## Step 4: setting up the CI/CD pipeline

In the previous step, we leveraged Azure ML service to keep track of the model execution and deployment. In this step, we're automating the entire process into a CI/CD pipeline using Azure DevOps.

[Setting up the CI/CD pipeline in Azure DevOps](https://github.com/Microsoft/MLOpsPython)
