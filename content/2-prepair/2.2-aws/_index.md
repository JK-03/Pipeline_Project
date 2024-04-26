---
title : "AWS"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### AWS Configuration
#### Run AWS CLI in container:
Run docker compose: 
```dockercompose
 docker-compose run --rm aws --version 
```
![22](/cicd-ws/images/2-prepair/2.2-aws/1.png)

#### Create AWS Keypair to access AWS Instances

Create user: **tf-cli-keypair.pem**
```dockercompose 
docker-compose run --rm aws ec2 create-key-pair --key-name tf-cli-keypair --query 'KeyMaterial' --output text > tf-cli-keypair.pem
```
![22](/cicd-ws/images/2-prepair/2.2-aws/5.png)

#### Create AWS Account for Terraform use AWS CLI

Create user: **tf-cli**
```dockercompose 
 docker-compose run --rm aws iam create-user --user-name tf-cli
```
AWS Checking Keypair:
![22](/cicd-ws/images/2-prepair/2.2-aws/2.png)

Create Access Key & export to local
```dockercompose 
 docker-compose run --rm aws iam create-access-key --user-name tf-cli > tf_cli-access_key.json
```
![22](/cicd-ws/images/2-prepair/2.2-aws/3.png)

Create policy and allow access EC2 and Limit Region 
  - Create a custom policy file: **ec2-limited-access-policy.json**
            
```policy 
 {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "ec2:*",
            "Resource": "*",
            "Condition": {
                "StringEquals": {
                    "ec2:Region": "ap-southeast-1"
                }
            }
        }
    ]
}
```
 - Create a IAM policy: **EC2FullAccessAPSouthEast1**

```dockercompose 
 docker-compose run --rm aws iam create-policy --policy-name EC2FullAccessAPSouthEast1 --policy-document file://ec2-limited-access-policy.json
```
 - Attach the Policy to the IAM User: (**tf-cli**)

```dockercompose 
 docker-compose run --rm aws iam attach-user-policy --user-name tf-cli --policy-arn arn:aws:iam::637423373411:policy/EC2FullAccessAPSouthEast1
```

AWS Checking User:
![22](/cicd-ws/images/2-prepair/2.2-aws/4.png?featherlight=false&width=90pc)