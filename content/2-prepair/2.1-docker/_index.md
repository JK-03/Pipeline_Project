---
title : "Docker"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---


#### Docker & Docker Compose status:
Run commands:
```docker
 docker --version 
```
```dockercompose
 docker-compose --version 
```
![22](/cicd-ws/images/2-prepair/2.1-docker/4.png)

#### Create Docker Compose file
-  **docker-compose.yml**
```Docker-compose
version: '3'
services:

# Terraform
  terraform:
    image: hashicorp/terraform:latest
    volumes:
      - .:/terraform
    working_dir: /terraform

# AWS CLI'
  aws:
    image: anigeo/awscli
    environment:
      AWS_ACCESS_KEY_ID: "${AWS_ACCESS_KEY_ID}"
      AWS_SECRET_ACCESS_KEY: "${AWS_SECRET_ACCESS_KEY}"
      AWS_REGION: "${AWS_REGION}"
      AWS_DEFAULT_REGION: ap-southeast-1
    volumes:
      - $PWD:/app
    working_dir: /app

```
