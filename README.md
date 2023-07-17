# Challenge

Deploy Azure resources by using Terraform

## Objective

Requirements for the Terraform Script:

1. Creates a Resource Group
2. Creates a Virtual Network and Subnet
3. Attaches a Network Security Group to the Subnet
4. Creates a Key Vault
5. Creates a Storage Account and Container
6. Tags all resources with the key "Owner" and value = <your name>
7. Storage Account should be locked down so it is only accessible on the above VNET and your IP.
8. Key Vault should be locked down so it is only accessible on the above VNET and your IP.
9. Once you deploy the Infrastructure, move the Terraform state file to the above Storage Account using the Terraform script.

## Tools

These are the tools I used for the completion of this challenge with their corresponding versions

| Plugin | Version |
| ------ | ------ |
| Azure | 3.64.0 |
| Terraform | 1.5.0 |
| Git | 2.34.1 |

## Instructions

### Step 1:

Comment out the backend block and Save in the **main.tf** file

```
#terraform {
#  backend "azurerm" {
#    resource_group_name  = "tranzact_RG"
#    storage_account_name = "tranzactcbalcazar4585"
#    container_name       = "tranzactcbalcazar4585container"
#    key                  = "terraform.tfstate"
#  }
#} 
```

### Step 2:

Set the parameter **ip_rules** with your current public ip in the following modules

- networking_module
- storage_module

### Step 3:

```
terraform init
```

### Step 4:

```
terraform plan
```

### Step 5:

```
terraform apply
```
### Step 6:

Uncomment backend block and Save in the **main.tf** file

```
terraform {
  backend "azurerm" {
    resource_group_name  = "tranzact_RG"
    storage_account_name = "tranzactcbalcazar4585"
    container_name       = "tranzactcbalcazar4585container"
    key                  = "terraform.tfstate"
  }
} 
```

### Step 7:

```
terraform init
```