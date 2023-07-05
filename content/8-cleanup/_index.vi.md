---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

#### Dọn dẹp tài nguyên
Chúng ta sẽ dọn dẹp tài nguyên theo thứ tự như sau:

#### Xóa Auto Scaling Group

- Truy cập **EC2 Management Console**
- Trên thanh điều hướng bên trái, chọn **Auto Scaling Groups**
- Chọn **Auto Scaling Group** liên quan tới bài lab.
- Click **Delete**
- Gõ delete vào ô trống và nhấn delete

#### Xóa Load Balancer

- Truy cập **EC2 Management Console**
- Trên thanh điều hướng bên trái, chọn **Load Balancers**
- Chọn **Load Balancer** liên quan tới bài lab.
- Click **Actions**
- Click **Delete**

#### Xóa Target Group

- Truy cập **EC2 Management Console**
- Trên thanh điều hướng bên trái, chọn **Target Groups**
- Chọn **Target Group** liên quan tới bài lab.
- Click **Actions**
- Click **Delete**
- Click **Yes, delete**

#### Xóa Launch Template

- Truy cập **EC2 Management Console**
- Trên thanh điều hướng bên trái, chọn **Launch Templates**
- Select **Launch Template** liên quan tới bài lab.
- Click **Actions**
- Click **Delete template**
- Gõ delete vào ô trống và nhấn **delete**

#### Xóa AMI

- Truy cập **EC2 Management Console**
- Trên thanh điều hướng bên trái, chọn **AMIs**
- Chọn **AMI** liên quan tới bài lab.
- Click **Actions**
- Click **Deregister**
- Click **Continue**

#### Terminate EC2 instance

- Truy cập **EC2 Management Console**
- Trên thanh điều hướng bên trái, chọn **Intances**
- Chọn tất cả **EC2 Instance** liên quan tới bài lab.
- Click **Actions**
- Click **Manage Instance State**
- Chọn **Terminate**
- Click **Change State**

#### Xoá DB Instance

- Truy cập **RDS Management Console**
- Trên thanh điều hướng bên trái, chọn **Databases**
- Chọn tất cả **DB Instance** liên quan tới bài lab.
- Click **Actions**
- Click **Delete**
- Bỏ chọn **Create final snapshot?** và chọn **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available**
- Gõ **delete me** vào ô trống.
- Click **Delete**

#### Xóa Security Group

- Truy cập **EC2 Management Console**
- Trên thanh điều hướng bên trái, chọn **Security Groups**
- Chọn tất cả **Security Groups** liên quan tới bài lab.
- Click **Actions**
- Click **Delete security groups**
- Click **Delete**