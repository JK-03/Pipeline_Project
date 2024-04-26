---
title : "Terraform"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Run Terraform in containter:
Run docker compose: 
```dockercompose
 docker-compose run --rm terraform version
```
![23](/cicd-ws/images/2-prepair/2.3-terraform/1.png)

#### Terraform configuration

Terraform provider aws:  **versions.tf**

```dockercompose
 terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 4.16"
    }
  }

  required_version = ">= 1.2.0"
}
```
Security credential variables:  **variables.tf**

```dockercompose
variable "access_key" {
  type        = string
  sensitive   = true
}

variable "secret_key" {
  type        = string
  sensitive   = true
}

variable "region" {
  type        = string
  default     = "ap-southeast-1"
}
```


Terraform init:
```dockercompose
 docker-compose run --rm terraform init
```
![23](/cicd-ws/images/2-prepair/2.3-terraform/2.png)