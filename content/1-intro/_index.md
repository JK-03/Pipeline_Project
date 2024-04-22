---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

# Infrastructure As Code with Terraform and AWS

#### Overview

HashiCorp Terraform is an infrastructure as code tool that lets you define both cloud and on-prem resources in human-readable configuration files that you can version, reuse, and share.

You can then use a consistent workflow to provision and manage all of your infrastructure throughout its lifecycle. 

Terraform can manage low-level components like compute, storage, and networking resources, as well as high-level components like DNS entries and SaaS features.

In this workshop we will use Terraform with AWS to create VPC, Subnet, EC2 , Route table, Internet gateway, Security group

![1](/ws-0001/images/1/terraform.png?featherlight=false&width=90pc)

#### Content

1. [Introduction](/ws-0001/1-intro/)
2. [Prepairation](/ws-0001/2-prepair/)
3. [Terraform Configure](3-tfonfig/)
4. [Resource Cleanup](4-cleanup/)