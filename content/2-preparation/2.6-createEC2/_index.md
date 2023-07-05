---
title : "Create EC2 Instance"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 2.6 </b> "
---

#### Create EC2 instance
1. Go to [AWS Management Console](https://aws.amazon.com/console/)

    - Find **EC2**
    - Select **EC2**
![Create EC2 instance](/images/2.preparation/036-CreateEC2.png?width=90pc)

2. In the **EC2** interface

    - Select **Instances**
    - Select **Launch instances**
![Create EC2 instance](/images/2.preparation/037-CreateEC2.png?width=90pc)

3. Name instance, enter ```FCJ-Management```
![Create EC2 instance](/images/2.preparation/038-CreateEC2.png?width=90pc)

4. Made for **AMI**

    - Select **Quick Start**
    - Select **Amazon Linux**

![Create EC2 instance](/images/2.preparation/039-CreateEC2.png?width=90pc)

5. Select **Instance type**

    - Select **t2.micro**
    - Select **Create new key pair**
![Create EC2 instance](/images/2.preparation/040-CreateEC2.png?width=90pc)

    - Configure key pair.
![Create EC2 instance](/images/2.preparation/041-CreateEC2.png?width=90pc)

6. Configure **Network**
![Create EC2 instance](/images/2.preparation/042-CreateEC2.png?width=90pc)

    - **VPC**, select the *created VPC*.
    - **Subnet**, select **Public subnet**.
    - Check if **Auto-assign public IP?**. If you have not reviewed the step of allocating public IP in the step of creating VPC.
    - Select Select existing security group and then select *FCJ-Management-SG*
![Create EC2 instance](/images/2.preparation/043-CreateEC2.png?width=90pc)

7. Select **Launch instance**
![Create EC2 instance](/images/2.preparation/044-CreateEC2.png?width=90pc)

8. Successfully initialized instance and select **View all instances**
![Create EC2 instance](/images/2.preparation/045-CreateEC2.png?width=90pc)

9. View instance details and note **Public IPv4 address** to make the connection in the next step.
![Create EC2 instance](/images/2.preparation/046-CreateEC2.png?width=90pc)