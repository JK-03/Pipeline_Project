---
title : "Terraform"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

## Terraform code to deployment AWS

- **Review Terraform configure files** :
    - **main.tf** :
         Resource blocks describe infrastructure objects like VPCs, subnets, route tables, and gateways
   ![23](/ws-0001/images/2-prepair/2.3-terraform/5-main.png)

    - **provider.tf**:
        Enables Terrafrom to interact with cloud providers and other APIs
    ![23](/ws-0001/images/2-prepair/2.3-terraform/2-provider.png)

    - **versions.tf**:
        Sets version constaints for Terraform and optionally maps provides to a source address and version constaint
    ![23](/ws-0001/images/2-prepair/2.3-terraform/1-versions.png)

    - **terraform.tfvars**:
        To set lots of variables, it is more convenient to specify their values in a variable definitions file
    ![23](/ws-0001/images/2-prepair/2.3-terraform/4-tfvars.png)

    - **variables.tf**
        Input variables define reusable values and work like function arguments in general-purpose programming languages
    ![23](/ws-0001/images/2-prepair/2.3-terraform/3-variables.png)

