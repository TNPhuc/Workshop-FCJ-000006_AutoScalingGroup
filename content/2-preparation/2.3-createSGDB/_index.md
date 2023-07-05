---
title : "Create Security Group DB"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Create a security group for the Database instance.
1. We create a Security group for the Database instance. To ensure security, do not configure the application’s Security group together.

    - Select **Security Group**
    - Select **Create security group**
![Create SG](/images/2.preparation/014-CreateSGDB.png?width=90pc)

2. Practice configuration **security group**

    - Security Group name, enter ```FCJ-Management-DB-SG```
    - Description, enter ```Security Group for DB instance```
    - Select the newly created VPC
![Create SG](/images/2.preparation/015-CreateSGDB.png?width=50pc)

3. Configure Inbound rules

    - Select **Add rule**
    - Select **MYSQL/Aurora** port *3306*
    - Then select Source as **FCJ-Management-SG**
    - Select **Create security group**
    ![Create SG](/images/2.preparation/016-CreateSGDB.png?width=50pc)
    ![Create SG](/images/2.preparation/017-CreateSGDB.png?width=50pc)

4. Finish creating **Security group** for the database.
![Create SG](/images/2.preparation/018-CreateSGDB.png?width=90pc)