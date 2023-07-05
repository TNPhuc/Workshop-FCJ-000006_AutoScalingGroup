---
title : "Preparation"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

#### Preparation
In this exercise, we need to prepare some services to be able to deploy the FCJ Management application using Auto Scaling Group with Elastic Load Balancer. In general, we will deploy the ShareNote application according to the following architecture:

![ImageArchitecture](/images/2.preparation/000-preparation.png?width=50pc)

#### Content
1. [Create VPC](2.1-createVPC/)
2. [Create Security Group for FCJ Management instance](2.2-createSG/)
3. [Create Security Group for DB instance](2.3-createSGDB/)
4. [Create DB Subnet Group](2.4-createDBSG/)
5. [Create DB instance](2.5-createDBinstance/)
6. [Create EC2 instance](2.6-createEC2/)
7. [Connect EC2 instance](2.7-connectingEC2/)
8. [Connect DB instance](2.8-connectDB/)
9. [Deploy Application](2.9-depFCJmanaapp/)
10. [Initialize AMI from Virtual Machine](2.10-LaunchAMI/)