# Create a new instance of Spinnaker running on a VM in Azure.  

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fscotmoor%2Fazure-quickstart-templates%2Fmaster%2Fspinnaker-azure-trial%2Fazuredeploy.json" target="_blank">
<img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fscotmoor%2Fazure-quickstart-templates%2Fmaster%2Fspinnaker-azure-trial%2Fazuredeploy.json" target="_blank">
<img src="http://armviz.io/visualizebutton.png"/>
</a>

This template allows you to create a new VM with an instance of Spinnaker installed and ready to configure for deploying your application to Azure.

The template will create two VMs in your subscription. The first is solely responsible for handling setup operations. Once the deployment has completed you may remove this VM and it's associated resoures.
The second VM wil be the actual instance of Spinnaker. Once the second VM has beend deployed, you will need to remote into the machine, via ssh, to complete the configuration of Spinnaker (see steps below).  

```PowerShell
.\Deploy-AzureResourceGroup.ps1 -ResourceGroupLocation 'eastus' -ArtifactsStagingDirectory '[foldername]'
```
```bash
azure-group-deploy.sh -a [foldername] -l eastus -u
```
If your sample has artifacts that need to be "staged" for deployment (Configuration Scripts, Nested Templates, DSC Packages) then set the upload switch on the command.
You can optionally specify a storage account to use, if so the storage account must already exist within the subscription.  If you don't want to specify a storage account
one will be created by the script (think of this as "temp" storage for AzureRM) and reused by subsequent deployments.

```PowerShell
.\Deploy-AzureResourceGroup.ps1 -ResourceGroupLocation 'eastus' -ArtifactsStagingDirectory '100-STARTER-TEMPLATE-with-VALIDATION' -UploadArtifacts 
```
```bash
azure-group-deploy.sh -a 100-STARTER-TEMPLATE-with-VALIDATION -l eastus -u
```

This template deploys a **solution name**. The **solution name** is a **description**

`Tags: Tag1, Tag2, Tag3`

## Solution overview and deployed resources

This is an overview of the solution

The following resources are deployed as part of the solution

#### Resource provider 1

Description Resource Provider 1

+ **Resource type 1A**: Description Resource type 1A
+ **Resource type 1B**: Description Resource type 1B
+ **Resource type 1C**: Description Resource type 1C

#### Resource provider 2

Description Resource Provider 2

+ **Resource type 2A**: Description Resource type 2A

#### Resource provider 3

Description Resource Provider 3

+ **Resource type 3A**: Description Resource type 3A
+ **Resource type 3B**: Description Resource type 3B

## Prerequisites

Decscription of the prerequistes for the deployment

## Deployment steps

You can click the "deploy to Azure" button at the beginning of this document or follow the instructions for command line deployment using the scripts in the root of this repo.

## Usage

#### Connect

How to connect to the solution

#### Management

How to manage the solution

## Notes

Solution notes