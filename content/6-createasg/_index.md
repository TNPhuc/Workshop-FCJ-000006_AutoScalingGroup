---
title : "Create Auto Scaling Group"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

#### Create Auto Scaling Group

In this section, we will implement an Auto Scaling Group for the FCJ Management application to ensure our application will be deployed with high availability, and potentially increase the number of EC2 instances when users visit. into the boost system.

1. Access to **EC2**

    - Select **Auto Scaling Groups**
    - Select **Create Auto Scaling group**

![Auto Scaling Group](/images/6.asg/0001.png?width=90pc)

2. **Auto Scaling Group** name, enter ```FCJ-Management-ASG```
![Auto Scaling Group](/images/6.asg/0002.png?width=90pc)

3. Configure the template

    - **Launch template**. select **FCJ-Management-template**
    - Select **Next**

![Auto Scaling Group](/images/6.asg/0003.png?width=90pc)

4. Configure **Network**

    - **VPC**, select created.
    - Select **AZ and subnet**

![Auto Scaling Group](/images/6.asg/0004.png?width=90pc)

5. Select **Next**

![Auto Scaling Group](/images/6.asg/0005.png?width=90pc)

6. Configure **Load balancing**

    - Select **Attach to an existing load balancer**
    - Select **Choose from your load balancer target groups**
    - Select **FCJ-Management-TG**

![Auto Scaling Group](/images/6.asg/0006.png?width=90pc)

7. Select **Next**

![Auto Scaling Group](/images/6.asg/0007.png?width=90pc)

8. Configure group size and scaling policy.

    - Desired capacity: Enter 1. (Default)
    - Minimum capacity: Enter 1. (Default)
    - Maximum capacity: Enter 3.

![Auto Scaling Group](/images/6.asg/0008.png?width=90pc)

9. Under **Scaling policies** - optional: Select this exercise to make it easier for the next step to be checked. You can completely set the resource scaling policy according to your needs.

    - Select **Target tracking scaling policy**
    - **Scaling policy name**, enter ```Target Tracking Policy```
    - **Metric type**, select **Application Load Balancer request count per target**
    - **Target group**, enter ```FCJ-Management```
    - **Target value**, enter 30

![Auto Scaling Group](/images/6.asg/0009.png?width=90pc)

10. Select **Next**

![Auto Scaling Group](/images/6.asg/00010.png?width=90pc)

11. Select **Create a topic**

![Auto Scaling Group](/images/6.asg/00011.png?width=90pc)

12. Configure **Add notifications**. Select **Next**

![Auto Scaling Group](/images/6.asg/00012.png?width=90pc)

- Check email and **Confirm subscription**

![Auto Scaling Group](/images/6.asg/00013.png?width=90pc)
![Auto Scaling Group](/images/6.asg/00014.png?width=90pc)

13. Select **Create Auto Scaling group**

![Auto Scaling Group](/images/6.asg/00015.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00016.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00017.png?width=90pc)

14. Complete creation **Auto Scaling groups**

![Auto Scaling Group](/images/6.asg/00018.png?width=90pc)

15. The initialization of Auto Scaling Group will be done, the newly created Auto Scaling Group will be displayed in the list, and you can select it to view detailed information.

    - We can track existing EC2 instances in Auto Scaling Group on the **Instance management** page. Instances with InService status are ready-to-go instances.

![Auto Scaling Group](/images/6.asg/00019.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00020.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00021.png?width=90pc)