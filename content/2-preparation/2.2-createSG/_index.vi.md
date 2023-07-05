---
title : "Tạo Security Group"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Security Group cho FCJ Management
1. Chúng ta sẽ tạo Security group cho ứng dụng.

    - Trong giao diện VPC, chọn **Security Group**
    - Chọn **Create security group**
![Create SG](/images/2.preparation/009-CreateSG.png?width=90pc)

2. Thực hiện cấu hình Security Group

    - **Security group name**, nhập ```FCJ-Management-SG```
    - **Description**, nhập ```Security Group for FCJ Management```
    - **VPC**, chọn VPC vừa tạo.
![Create SG](/images/2.preparation/010-CreateSG.png?width=50pc)

3. Cấu hình **Inbound rules**

    - Đầu tiên phải cấu hình **SSH** port *22* và **Source: MyIP** để có thể truy cập vào instance.
    - Tiếp theo là **HTTP** port *80*.
    - **Custom TCP** port *5000* dành cho **FCJ Management**
    - **HTTPS** port *443*.
![Create SG](/images/2.preparation/011-CreateSG.png?width=50pc)

4. Kiểm tra **Outbound rules** và chọn **Create security group**
![Create SG](/images/2.preparation/012-CreateSG.png?width=50pc)

5. Hoàn thành tạo **Security Group** cho ứng dụng FCJ Management. Kiểm tra thông tin chi tiết Security Group.

![Create SG](/images/2.preparation/013-CreateSG.png?width=90pc)