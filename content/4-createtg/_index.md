---
title : "Create Target Group"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### Create Target Group

1. Access **EC2** interface

    - Select **Target Groups**
    - Select **Create target group**

![Deploy app](/images/4.createtg/001-tg.png?width=90pc)

2. Make a configuration

    - Select **Instances**

![Deploy app](/images/4.createtg/002-tg.png?width=90pc)

3. On the **Specify group details** page, set the following parameters for **target group:**

    - **Target group name:** Enter the name of the target group (eg **FCJ-Management-TG**).
    - **Protocol**: *HTTP*.
    - **Port: 5000** (Port used by *FCJ Management*).
    - The remaining items leave the default.

![Deploy app](/images/4.createtg/003-tg.png?width=90pc)

4. Select **Next**

![Deploy app](/images/4.createtg/004-tg.png?width=90pc)

5. In the **Available instances** interface

    - Select **FCJ-Management** instance
    - Select port **5000**
    - Select **Include as pending below** (if not selected when accessing with DNS Load Balancer will get an error **HTTP 503: Service unavailable**)
    - Review
    - Select **Create target group**

![Deploy app](/images/4.createtg/005-tg.png?width=90pc)

6. In the **Register pending targets only** interface, select **Continue**

![Deploy app](/images/4.createtg/006-tg.png?width=90pc)

7. Finish creating **Target group**

![Deploy app](/images/4.createtg/007-tg.png?width=90pc)