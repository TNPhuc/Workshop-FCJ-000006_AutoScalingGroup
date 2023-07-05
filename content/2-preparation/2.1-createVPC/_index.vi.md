---
title : "Tạo VPC"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Tạo VPC
1. Truy cập vào [AWS Management Console](https://eu-central-1.console.aws.amazon.com/console/home?region=eu-central-1#)

    - Tìm **VPC**
    - Chọn **VPC**
![Create VPC](/images/2.preparation/001-CreateVPC.png?width=90pc)

2. Trong giao diện **VPC**

    - Chọn **Your VPCs**
    - Chọn **Create VPC**
![Create VPC](/images/2.preparation/002-CreateVPC.png?width=90pc)

3. Trong giao diện **Create VPC**
    - Chọn **VPC and more**
    - **Name**, nhập tên VPC của bạn. Trong bài lab này, ta đặt tên là aws-lab
    - **IPv4 CIDR block**, nhập **10.0.0.0/16**
![Create VPC](/images/2.preparation/003-CreateVPC.png?width=90pc)

4. Chọn **Create VPC**
![Create VPC](/images/2.preparation/004-CreateVPC.png?width=90pc)

5. Tạo VPC thành công và chọn **View VPC**
![Create VPC](/images/2.preparation/005-CreateVPC.png?width=90pc)

6. Thông tin chi tiết VPC vừa tạo.

7. Thực hiện cấp phát IP public.

    - Chọn **Subnets**
    - Chọn **public subnet**
    - Chọn **Edit subnet settings**
![Create VPC](/images/2.preparation/006-CreateVPC.png?width=90pc)

8. Chọn **Enable auto-assign public IPv4 address**. Chọn **Save**
![Create VPC](/images/2.preparation/007-CreateVPC.png?width=90pc)

9. Kiểm tra đã cấp phát thành công.
![Create VPC](/images/2.preparation/008-CreateVPC.png?width=90pc)

10. Thực hiện cấp phát cho Public subnet còn lại (làm tương tự).