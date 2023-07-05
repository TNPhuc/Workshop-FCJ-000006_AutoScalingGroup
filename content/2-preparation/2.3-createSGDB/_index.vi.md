---
title : "Tạo Security Group DB"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Tạo security group cho Database instance.
1. Chúng ta tạo Security group cho Database instance. Để đảm bảo bảo mật nên không cấu hình chung Security group của ứng dụng.

    - Chọn **Security Group**
    - Chọn **Create security group**
![Create SG](/images/2.preparation/014-CreateSGDB.png?width=90pc)

2. Thực hành cấu hình **security group**

    - **Security Group name**, nhập ```FCJ-Management-DB-SG```
    - **Description**, nhập ```Security Group for DB instance```
    - Chọn VPC vừa tạo
![Create SG](/images/2.preparation/015-CreateSGDB.png?width=50pc)

3. Cấu hình **Inbound rules**

    - Chọn **Add rule**
    - Chọn **MYSQL/Aurora** port *3306*
    - Sau đó chọn Soure là **FCJ-Management-SG**
    - Chọn **Create security group**

    ![Create SG](/images/2.preparation/016-CreateSGDB.png?width=50pc)
    ![Create SG](/images/2.preparation/017-CreateSGDB.png?width=50pc)

4. Hoàn thành tạo **Security group** cho database.

![Create SG](/images/2.preparation/018-CreateSGDB.png?width=90pc)