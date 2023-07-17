# Challenge

Deploy Azure resources by using Terraform

## Objective

> Requirements for the Terraform Script:
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