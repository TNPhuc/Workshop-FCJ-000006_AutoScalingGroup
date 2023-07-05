---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Introduce
In this exercise, we will deploy the application with Auto Scaling Group to ensure the scalability of the application according to the needs of the user. In addition, we will also implement a Load Balancer to balance the load and coordinate user access requests to our Application Tier.

Make sure you go through the [Deploying FCJ Management Application on a Windows/AmazonLinux Virtual Machine] document and understand how to deploy the application on the virtual machine. We will need to use the virtual machine deployed FCJ Management for mass deployment and scaling in the Auto Scaling Group.

#### Auto Scaling Group
**Auto Scaling Group** is a group of EC2 Instances. This group can scale the number of EC2 Instance members according to the scaling policy you set.

#### Launch Template
**Launch Template** is a feature that helps you create a template for the initialization of EC2 Instances. As a result, you can streamline and simplify the creation of EC2 Instances for the Auto Scaling service.

#### Load Balancer
**Load Balancer** is a tool that can distribute exchanged data traffic to AWS resources (specifically, EC2 Instances in this lab) in the Target Group.

#### Target Group
**Target Group** is a group of AWS resource elements that will receive data traffic delivered and transported by the Load Balancer.

In this exercise, we will deploy the application with Auto Scaling Group to ensure the scalability of the application according to the needs of the user. In addition, we will also implement a Load Balancer to balance the load and coordinate user access requests to our Application Tier.

Make sure you go through the documentation Deploying FCJ Management Applications on Windows/AmazonLinux Virtual Machines and understand how to deploy the application on the virtual machine. We will need to use FCJ Management deployed virtual machine for mass deployment and scaling in Auto Scaling Group.

![ImageArchitecture](/images/1.introduction/000.png?width=50pc)
