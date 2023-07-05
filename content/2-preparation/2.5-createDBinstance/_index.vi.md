---
title : "Tạo DB instance"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

#### Tạo DB instance
1. Truy cập vào **AWS Management Console**

    - Tìm **RDS**
    - Chọn **RDS**
![Create DB instance](/images/2.preparation/024-CreateDB.png?width=90pc)

2. Trong giao diện **RDS** 

    - Chọn **Databases**
    - Chọn **Create database**
![Create DB instance](/images/2.preparation/025-CreateDB.png?width=90pc)

3. Chọn phương thức tạo **database**

    - Chọn **Standard create**
![Create DB instance](/images/2.preparation/026-CreateDB.png?width=90pc)

4. Cấu hình **Engine** database

    - Chọn **MySQL**
![Create DB instance](/images/2.preparation/027-CreateDB.png?width=90pc)

5. Cấu hình **Template**

    - Chọn **Dev/Test**
    - Đối với **Availability and durability**, chọn **Mutil-AZ DB instance**
![Create DB instance](/images/2.preparation/028-CreateDB.png?width=90pc)

6. Tiếp theo, thực hiện cài đặt chi tiết

    - **DB instance identifier**, nhập ```fcj-management-db-instance```
    - **Master user**, nhập **admin**
    - **Master password**, nhập tùy ý của bạn ( trong bài lab, nhập ```phuc2002```)
    - **Confirm password**, nhập lại password 1 lần nữa.
![Create DB instance](/images/2.preparation/029-CreateDB.png?width=90pc)

7. Thực hiện cấu hình network cho db instance

    - **Network type**, chọn **IPv4**
    - **VPC**, chọn **asg-vpc** đã tạo
    - **Subnet group**, chọn subnet group đã tạo.
    - **VPC security group**, chọn **Choose existing**
    - **Security Group**, chọn **FCJ-Management-DB-SG** (tránh nhầm lẫn với SG của web).
![Create DB instance](/images/2.preparation/030-CreateDB.png?width=90pc)

8. Khởi tạo Database với tên **awsuser**, còn lại để mặc định.
![Create DB instance](/images/2.preparation/031-CreateDB.png?width=90pc)

    - Lưu ý: Ở tùy chọn Deletion protection, giá trị mặc định là Enable giúp bảo vệ cơ sở dữ liệu khỏi bị vô tình xóa (Protects the database from being deleted accidentally). Tuy nhiên, trong bài lab này, ta Disable Deletion protection để dễ dọn dẹp tài nguyên vào cuối bài lab.
9. Kiểm tra lại và chọn **Create database**
![Create DB instance](/images/2.preparation/032-CreateDB.png?width=90pc)

10. Khởi tạo DB instance trong 10 phút. Khi **Status** chuyển sang **Available**, là hoàn thành.

    - Chọn vào **DB instance** vừa tạo.
![Create DB instance](/images/2.preparation/033-CreateDB.png?width=90pc)

11. Trong giao diện **Connectivity & security**

    - Lưu trữ giá trị **Endpoint**
    - Kiểm tra port **port** *3306*
![Create DB instance](/images/2.preparation/034-CreateDB.png?width=90pc)
![Create DB instance](/images/2.preparation/035-CreateDB.png?width=90pc)