---
title : "VPC & Subnet"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---
## Run Terraform

### Terraform init
- Command: **docker-compose run --rm terraform init**

![31](/ws-0001/images/3-tfconfig/1-tfinit.png)

### Terraform plan

- Command: **docker-compose run --rm terraform plan**
- Input AWS **Access and Secret key**
![31](/ws-0001/images/3-tfconfig/2-tfplan-1.png)
![31](/ws-0001/images/3-tfconfig/2-tfplan-2.png)
![31](/ws-0001/images/3-tfconfig/2-tfplan-3.png)

### Terraform apply
- Command: **docker-compose run --rm terraform apply**
- Input AWS **Access and Secret key**
![31](/ws-0001/images/3-tfconfig/3-tfapply-1.png)
![31](/ws-0001/images/3-tfconfig/3-tfapply-2.png)
![31](/ws-0001/images/3-tfconfig/3-tfapply-3.png)
![31](/ws-0001/images/3-tfconfig/3-tfapply-4.png)


## AWS Console
- Checking VPC & Subnet:

![31](/ws-0001/images/3-tfconfig/4-1-awsvpc.png)
![31](/ws-0001/images/3-tfconfig/4-2-awssubnet.png)
   

