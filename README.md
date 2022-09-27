# Azure Synapse End-End Demo

This repository provides one-click infrastructure and artifact deployment for Azure Synapse Analytics to get you started with Big Data Analytics on a 
large sized Health Care sample data. You will learn how to ingest, process, and serve large volumes of data using various components of Synapse.

## Deploy Azure Synapse Demo in Your Azure Environment

### Pre-requisites to Deploy Synapse end-to-end Demo

* You must have a github account
* You must have an active azure subscription

### Deployment Steps
Please follow the below steps to successfully deploy a Synapse workspace and its artifacts on your Azure subscription

* Fork microsoft/AzureSynapseEndToEndDemo project to your local github account. Make sure to check "Copy the main branch only".

    ![Forking](/Images/Forking.gif)

* Once you fork the AzureSynapseEndToEndDemo project to your github account, please click on **Deploy to Azure** button to start the deployment

    [![Deploy To Azure](/Images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2FAzureSynapseEndToEndDemo%2Fmain%2FARMTemplate%2Fazuredeploy.json)

* **Deploy to Azure** button takes you to https://ms.portal.azure.com/#create/Microsoft.Template webpage. Please provide subscription, resource group, region, storage account name, storage container name, workspace name, dedicated sql pool name, spark pool name, spark pool node size, sql administration username/password, sku (dedicated sql pool Data Warehouse Units), and github username parameter values.

    >*Note: The github username should be the target github account where you forked the project. Example: If https://github.com/microsoft/AzureSynapseEndToEndDemo is the github project url, then "microsoft" is github account name.*

* Click on the **Review + Create** button to trigger deployment validation. If deployment validation is successful, the single click deployment will deploy a Synapse Workspace, Dedicated SQL Pool, and Spark Pool. This deployment also enables git configuration so all the required artifacts for the end-to-end demo are committed to your user github project. This completes the Azure Synapse end-to-end code deployment step.

    >*Note: If deployment is incomplete, please look at the resource group activity log and find the latest deployment errors for more information*

### Demo Setup

First you will need to fill in a parameter before you can complete the exercises.  We need to provide the linked service to your storage account with the storage account name you chose during deployment.

![image](https://user-images.githubusercontent.com/59613090/192065803-c1c7ccd8-0ab5-487f-aeca-0bb957d9e24e.png)


Once you click on the linked service name it will open a panel where we can make changes and provide the correct parameter for our storage account.

![image](https://user-images.githubusercontent.com/59613090/192065892-d103a4b9-dffb-4198-8036-28ab4045382a.png)


Now that the parameter is complete you'll need to copy the demo data from our Microsoft repository to your data lake.  The data used in these exercises is synthetic health care data generated from [Synthea](https://synthea.mitre.org/) using their [Data Generator](https://github.com/synthetichealth/synthea/wiki/Basic-Setup-and-Running) and is all open source.  Alternatively, you could generate the data yourself and copy it to your lake.  To begin the copy you need to open the Data Prep Pipeline.

![image](https://user-images.githubusercontent.com/59613090/192581982-60376d3f-201c-4416-bd9e-57f41c81f285.png)


Once you have the pipeline open, you can execute it by adding a trigger and choosing the Trigger Now option.

![image](https://user-images.githubusercontent.com/59613090/192582378-b75f16e3-8426-41a8-9a8d-b0d9e9aacef1.png)


### Demo Execution

TBD
