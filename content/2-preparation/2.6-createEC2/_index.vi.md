---
title : "Tạo EC2 Instance"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 2.6 </b> "
---

#### Tạo EC2 instance
1. Truy cập vào [AWS Management Console](https://aws.amazon.com/console/)

    - Tìm **EC2**
    - Chọn **EC2**
![Create EC2 instance](/images/2.preparation/036-CreateEC2.png?width=90pc)

2. Tại giao diện **EC2**

    - Chọn **Instances**
    - Chọn **Launch instances**
![Create EC2 instance](/images/2.preparation/037-CreateEC2.png?width=90pc)

3. **Name instance**, nhập ```FCJ-Management```
![Create EC2 instance](/images/2.preparation/038-CreateEC2.png?width=90pc)

4. thực hiện cho **AMI**

    - Chọn **Quick Start**
    - Chọn **Amazon Linux**

![Create EC2 instance](/images/2.preparation/039-CreateEC2.png?width=90pc)

5. Chọn **Instance type**

    - Chọn **t2.micro**
    - Chọn **Create new key pair**
![Create EC2 instance](/images/2.preparation/040-CreateEC2.png?width=90pc)

    - Cấu hình **key pair**.
![Create EC2 instance](/images/2.preparation/041-CreateEC2.png?width=90pc)

6. Cấu hình **Network**
![Create EC2 instance](/images/2.preparation/042-CreateEC2.png?width=90pc)

    - **VPC**, chọn VPC đã tạo.
    - **Subnet**, chọn **Public subnet**.
    - Kiểm tra đã **Auto-assign public IP**chưa?. Nếu chưa xem lại bước cấp phát public IP ở bước tạo VPC.
    - Chọn **Select existing security group** rồi chọn *FCJ-Management-SG*
![Create EC2 instance](/images/2.preparation/043-CreateEC2.png?width=90pc)

7. Chọn **Launch instance**
![Create EC2 instance](/images/2.preparation/044-CreateEC2.png?width=90pc)

8. Khởi tạo instance thành công và chọn **View all instances**
![Create EC2 instance](/images/2.preparation/045-CreateEC2.png?width=90pc)

9. Xem chi tiết instance và ghi chú lại **Public IPv4 address** để thực hiện kết nối ở bước sau.
![Create EC2 instance](/images/2.preparation/046-CreateEC2.png?width=90pc)