---
title : "Create VPC"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Create VPC
1. Go to the [AWS Management Console](https://eu-central-1.console.aws.amazon.com/console/home?region=eu-central-1#)

    - Find **VPC**
    - Select **VPC**
![Create VPC](/images/2.preparation/001-CreateVPC.png?width=90pc)

2. In the **VPC** interface

    - Select **Your VPCs**
    - Select **Create VPC**
![Create VPC](/images/2.preparation/002-CreateVPC.png?width=90pc)

3. In the **Create VPC** interface

    - Select **VPC, subnets, etc,**
    - **Name**, enter your VPC name.
    - **IPv4 CIDR block**, enter **10.0.0.0/16**
![Create VPC](/images/2.preparation/003-CreateVPC.png?width=90pc)

4. Select **Create VPC**
![Create VPC](/images/2.preparation/004-CreateVPC.png?width=90pc)

5. Create VPC successfully and select **View VPC**
![Create VPC](/images/2.preparation/005-CreateVPC.png?width=90pc)

6. Details of the newly created VPC.

7. Implement public IP allocation.

    - Select **Subnets**
    - Select **public subnet**
    - Select **Edit subnet settings**
![Create VPC](/images/2.preparation/006-CreateVPC.png?width=90pc)

8. Select **Enable auto-assign public IPv4 address**. Select **Save**
![Create VPC](/images/2.preparation/007-CreateVPC.png?width=90pc)

9. Check that the allocation was successful.
![Create VPC](/images/2.preparation/008-CreateVPC.png?width=90pc)

10. Allocate the remaining Public subnet (do the same).