---
title : "Deploying FCJ Management Application With Auto Scaling Group"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# DEPLOYING FCJ MANAGEMENT APPLICATION WITH AUTO SCALING GROUP

#### Overview
 In this exercise, we will deploy the application with Auto Scaling Group to ensure the scalability of the application according to the needs of the user. In addition, we will also implement a Load Balancer to balance the load and coordinate user access requests to our Application Tier.

 Make sure you go through the [Deploying FCJ Management Application on a Windows/AmazonLinux Virtual Machine](https://000004.awsstudygroup.com/) document and understand how to deploy the application on the virtual machine. We will need to use the virtual machine deployed **FCJ Management** for mass deployment and scaling in the Auto Scaling Group. 
#### Auto Scaling Group
 **Auto Scaling Group** is a group of EC2 Instances. This group can scale the number of EC2 Instance members according to the scaling policy you set.
#### Launch Template
 **Launch Template** is a feature that helps you create a template for the initialization of EC2 Instances. As a result, you can streamline and simplify the creation of EC2 Instances for the Auto Scaling service.
#### Load Balancer
 **Load Balancer** is a tool that can distribute exchanged data traffic to AWS resources (specifically, EC2 Instances in this lab) in the Target Group.
#### Target Group
 **Target Group** is a group of AWS resource elements that will receive data traffic delivered and transported by the Load Balancer.

![ImageArchitecture](/images/000.png?width=50pc) 

#### Content
 1. [Introduction ](1-introduce/)
 2. [Preparation steps](2-preparation/)
 3. [Initialize Template](3-launchTemplate/)
 4. [Initialize Target Group](4-createtg)
 5. [Initialize Load Balancer](5-createlb)
 6. [Initialize Auto Scaling Group](6-createasg)
 7. [Check Result](7-checkresult)
 8. [Resources Cleanup](6-cleanup/)
