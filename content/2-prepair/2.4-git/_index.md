---
title : "Github"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

## Version control with Github
- Create Github Access Key : https://github.com/settings/tokens
  - Name: **github_token_ws**
  - Expiration:	90 days
  - Select scopes:
    - repo
    - workflow
    
- Clone Source form Github:
    git clone https://**token**@github.com/NoNotNonez/ws-0001.git
- Copy Source code to Github Repo:
    - cd /ws-0001/terraform
- Create **.gitignore**: 
  - to security and prevent important file upload to github
![24](/cicd-ws/images/2-prepair/2.4-git/1.png)

- Push Source code to Git Repo:
    - git status
    - git add .
    - git commit -m "Add Tf source"
    - git push 
![24](/cicd-ws/images/2-prepair/2.4-git/2.png)


