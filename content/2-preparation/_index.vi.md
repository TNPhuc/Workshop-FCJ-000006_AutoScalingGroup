---
title : "Các bước chuẩn bị"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

#### Các bước chuẩn bị
Trong bài thực hành này, chúng ta cần chuẩn bị một số dịch vụ để có thể tiến hành triển khai ứng dụng FCJ Management sử dụng Auto Scaling Group cùng với Elastic Load Balancer. Một cách tổng quan, chúng ta sẽ triển khai ứng dụng ShareNote theo kiến trúc như sau:
![ImageArchitecture](/images/2.preparation/000-preparation.png?width=50pc)

#### Content
1. [Tạo VPC](2.1-createVPC/)
2. [Tạo Security Group for FCJ Management instance](2.2-createSG/)
3. [Tạo Security Group for DB instance](2.3-createSGDB/)
4. [Tạo DB Subnet Group](2.4-createDBSG/)
5. [Tạo DB instance](2.5-createDBinstance/)
6. [Tạo EC2 instance](2.6-createEC2/)
7. [Kết nối EC2 instance](2.7-connectingEC2/)
8. [Kết nối DB instance](2.8-connectDB/)
9. [Triển khai ứng dụng](2.9-depFCJmanaapp/)
10. [Khởi tạo AMI từ máy ảo](2.10-LaunchAMI/)