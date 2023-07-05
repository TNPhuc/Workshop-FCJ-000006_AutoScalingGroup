---
title : "Create DB Subnet Group"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

#### Create DB Subnet Group
1. Go to [RDS](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1)

    - Select **Subnet groups**
    - Select **Create DB subnet group**
![Create SG](/images/2.preparation/019-CreateDBSG.png?width=90pc)

2. In the **Create DB subnet group** interface

    - **Name**, enter ```FCJ-Management-Subnet-Group```
    - **Description**, enter ```Subnet Group for FCJ Management```
    - Select the created VPC.
![Create SG](/images/2.preparation/020-CreateDBSG.png?width=50pc)

3. Configure **subnet**

    - Select the **AZ**
    - Select **subnet**
    - Select **Create**
![Create SG](/images/2.preparation/021-CreateDBSG.png?width=50pc)

4. Successfully create **DB Subnet Group**
![Create SG](/images/2.preparation/022-CreateDBSG.png?width=50pc)
![Create SG](/images/2.preparation/023-CreateDBSG.png?width=50pc)