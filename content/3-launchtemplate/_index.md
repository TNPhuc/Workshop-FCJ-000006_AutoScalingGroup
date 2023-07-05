---
title : "Launch Template"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

#### Launch Template
In this section, you will create a Launch Template using the AMI you created from the Amazon Linux 2 Instance in the previous step.

1. Access to **EC2**

    - Select **Launch Templates**
    - Select **Create launch template**

![Deploy app](/images/3.launchtemp/001-template.png?width=90pc)

2. In the **Create launch template** interface

    - **Launch template name**, enter ```FCJ-Management-template```
    - **Template version description**, enter ```Template for FCJ Management```

![Deploy app](/images/3.launchtemp/002-template.png?width=90pc)

3. Perform **AMI** selection

    - Select **My AMIs**
    - Select **Owned by me**
    - Select **FCJ-Management-AMI**

![Deploy app](/images/3.launchtemp/003-template.png?width=90pc)

4. Make **Instance type** selection

    - Select **t2.micro**
    - **Key pair**, select **aws-fcj-key** created when creating **EC2** instance.

![Deploy app](/images/3.launchtemp/004-template.png?width=90pc)

5. Configure **Network**

    - **Subnet**, select **public subnet**
    - **Firewall (Security Group)**, **select Select existing security group**
    - Select **FCJ-Management-SG**

![Deploy app](/images/3.launchtemp/005-template.png?width=90pc)

6. Check again and execute **Create launch template**

![Deploy app](/images/3.launchtemp/006-template.png?width=90pc)

7. Execute successfully and select **View launch templates**

![Deploy app](/images/3.launchtemp/007-template.png?width=90pc)

8. View the template just created.

![Deploy app](/images/3.launchtemp/008-template.png?width=90pc)