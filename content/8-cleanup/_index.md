---
title : "Clean up resources"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

#### Clean up resources
We will clean up resources in the following order:

#### Remove Auto Scaling Group

- Access **EC2 Management Console**
- On the left navigation bar, select **Auto Scaling Groups**
- Select **Auto Scaling Group** related to the lab.
- Click **Delete**
- Type delete in the empty box and press delete

#### Remove Load Balancer

- Access **EC2 Management Console**
- On the left navigation bar, select **Load Balancers**
- Select **Load Balancer** related to the lab
- Click **Actions**
- Click **Delete**

#### Remove Target Group

- Access **EC2 Management Console**
- On the left navigation bar, select **Target Groups**
- Select **Target Group** related to the lab.
- Click **Actions**
- Click **Delete**
- Click **Yes, delete**

#### Delete Launch Template

- Access **EC2 Management Console**
- On the left navigation bar, select **Launch Templates**
- Select **Launch Template** related to the lab.
- Click **Actions**
- Click **Delete template**
- Type delete in the empty box and press **delete**

#### Delete AMI

- Access **EC2 Management Console**
- On the left navigation bar, select **AMIs**
- Select **AMI** related to the lab.
- Click **Actions**
- Click **Deregister**
- Click **Continue**

#### Terminate EC2 instance

- Access **EC2 Management Console**
- On the left navigation bar, select **Intances**
- Select all **EC2 Instance** related to the lab
- Click **Actions**
- Click **Manage Instance State**
- Select **Terminate**
- Click **Change State**

#### Delete DB Instance

- Access the **RDS Management Console**
- On the left navigation bar, select **Databases**
- Select all **DB Instance** related to the lab.
- Click **Actions**
- Click **Delete**
- Uncheck **Create final snapshot? and select I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available**
- Type **delete me** in the empty box.
- Click **Delete**

#### Delete Security Group

- Access **EC2 Management Console**
- On the left navigation bar, select **Security Groups**
- Select all **Security Groups** related to the lab.
- Click **Actions**
- Click **Delete security groups**
- Click **Delete**