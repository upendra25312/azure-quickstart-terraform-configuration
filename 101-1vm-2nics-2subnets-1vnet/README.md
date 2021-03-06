# Terraform: 101-1vm-2nics-2subnets-1vnet 

## Multi-NIC Virtual Machine Creation using Two Subnets

## Description
This is a conversion of ARM template *[101-1vm-2nics-2subnets-1vnet](https://github.com/Azure/azure-quickstart-templates/tree/master/101-1vm-2nics-2subnets-1vnet)* from the repository *[azure\azure-quickstart-templates](https://github.com/Azure/azure-quickstart-templates)* to Terraform configuration.

This configuration creates a new VM with two NICs which connect to two different subnets within the same VNet, and it will deploy the following resources…

![output](resources.png)

> ### Note:
> If there is already the specified resource group exists then the script will not continue with the deployment. If you want to deploy the resources to the existing resource group, then import the resource group to state before deployment.

### Syntax
```
# To initialize the configuration directory
PS C:\Terraform\101-1vm-2nics-2subnets-1vnet> terraform init 

# To check the execution plan
PS C:\Terraform\101-1vm-2nics-2subnets-1vnet> terraform plan

# To deploy the configuration
PS C:\Terraform\101-1vm-2nics-2subnets-1vnet> terraform apply
```  

### Example
```
# Initialize
PS C:\Terraform\101-1vm-2nics-2subnets-1vnet> terraform init 

# Plan
PS C:\Terraform\101-1vm-2nics-2subnets-1vnet> terraform plan

var.adminPassword
Password for the Virtual Machine.
Enter a value: *********

<--- output truncated --->

# Apply
PS C:\Terraform\101-1vm-2nics-2subnets-1vnet> terraform apply 

var.adminPassword
Password for the Virtual Machine.
Enter a value: *********
```

### Output
```
azurerm_virtual_machine.avm-01: Creating...
azurerm_virtual_machine.avm-01: Still creating... [10s elapsed]

<--- output truncated --->

azurerm_virtual_machine.avm-01: Creation complete after 2m6s 

Apply complete! Resources: 14 added, 0 changed, 0 destroyed.

Outputs:

hostname = demodns2020.westus.cloudapp.azure.com
```

>Azure Cloud Shelll comes with terraform pre-installed and you deploy this configuration in Cloud Shell as well.
>
>[![](https://shell.azure.com/images/launchcloudshell.png "Launch Azure Cloud Shell")](https://shell.azure.com)