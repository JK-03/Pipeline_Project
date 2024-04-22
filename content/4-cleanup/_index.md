---
title : "Resource Cleanup"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---
## Clean up resources

We will proceed to delete the resources in the following order:

1. Terrafrom destroy:
 - Run command: **docker-compose run --rm terraform destroy**
 - Import **Secret & Access Key**
![4](/ws-0001/images/4-cleanup/1-tfdestroy.png)
![4](/ws-0001/images/4-cleanup/1-tfdestroy-2.png)
![4](/ws-0001/images/4-cleanup/1-tfdestroy-3.png)
      
2. Checking AWS Console:
![4](/ws-0001/images/4-cleanup/2-1-awsvpc.png)
![4](/ws-0001/images/4-cleanup/2-2-awssubnet.png)

3. Local Check:
 - Run command:
   - **docker system prune -a**
   - **docker images**
![4](/ws-0001/images/4-cleanup/3-dockerlocal.png)




