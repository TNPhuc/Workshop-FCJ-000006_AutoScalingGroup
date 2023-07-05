---
title : "Launch AMI from Virtual Machine"
date :  "`r Sys.Date()`" 
weight : 10
chapter : false
pre : " <b> 2.10 </b> "
---

#### Launch AMI from Virtual Machine

In this step, you will initialize an Amazon Machine Image (AMI) for the Amazon Linux Instance that was set up in the previous step. An AMI is a configuration snapshot of an EC2 Instance that allows you to deploy multiple EC2 Instances with the same configuration as the original EC2 Instance. AMI is commonly used inside Launch Template to template EC2 Instances.

1. Access to **EC2**

    - Select **Instances**
    - Select **FCJ-Management** instance
    - Select **Actions**
    - Select **Image and templates**
    - Select **Create image**

![Deploy app](/images/2.preparation/083-ami.png?width=90pc)

2. Configure **Template**

    - **Image name**, enter ```FCJ-Management-AMI```
    - **Image description**, enter ```AMI for FCJ-Management```
    - Select **Create image**

![Deploy app](/images/2.preparation/084-ami.png?width=90pc)

3. AMI initialization takes about 5 minutes. After 5 minutes we see **Status** switch to **Available**

![Deploy app](/images/2.preparation/085-ami.png?width=90pc)

We have completed the preparation steps for deploying FCJ Management with Auto Scaling Group.

![Deploy app](/images/2.preparation/086-ami.png?width=90pc)

In the next section, we will begin to initialize and deploy the main content of this exercise.