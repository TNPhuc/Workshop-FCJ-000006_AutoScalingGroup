---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Giới thiệu
Ở bài thực hành này, chúng ta sẽ tiến hành việc triển khai ứng dụng với Auto Scaling Group nhằm đảm bảo khả năng co giãn của ứng dụng đó theo nhu cầu của người truy cập. Thêm vào đó, chúng ta cũng sẽ triển khai Load Balancer nhằm cân bằng tải và điều phối các yêu cầu truy cập từ phía người dùng đến Application Tier của chúng ta.

 Hãy chắc chắn rằng bạn đã xem qua tài liệu [Triển khai Ứng dụng FCJ Management trên Máy ảo Windows/AmazonLinux](https://000004.awsstudygroup.com/) và nắm được cách triển khai ứng dụng trên máy ảo. Chúng ta sẽ cần sử dụng máy ảo được triển khai FCJ Management cho việc triển khai đồng loạt và mở rộng trong Auto Scaling Group.
#### Auto Scaling Group
 **Auto Scaling Group** (nhóm co giãn tự động) là một nhóm các EC2 Instance. Nhóm này có thể co giãn số lượng của các EC2 Instance thành viên theo chính sách co giãn (scaling policy) mà bạn đặt ra.
#### Launch Template
 **Launch Template** (khuôn mẫu khởi tạo) là một tính năng giúp bạn tạo khuôn mẫu cho việc khởi tạo các EC2 Instance. Nhờ thế, bạn có thể quy trình hóa và đơn giản hóa công tác khởi tạo các EC2 Instance cho dịch vụ Auto Scaling (co giãn tự động).
#### Load Balancer
 **Load Balancer** (máy cân bằng tải) là một công cụ có thể phân phối lưu lượng dữ liệu được trao đổi tới các tài nguyên AWS (cụ thể trong bài lab này là các EC2 Instances) trong Target Group.
#### Target Group
 **Target Group** (nhóm mục tiêu) là một nhóm những thành phần tài nguyên AWS sẽ nhận lưu lượng dữ liệu được phân phối và truyền tải bởi Load Balancer.

Ở bài thực hành này, chúng ta sẽ tiến hành việc triển khai ứng dụng với Auto Scaling Group nhằm đảm bảo khả năng co giãn của ứng dụng đó theo nhu cầu của người truy cập. Thêm vào đó, chúng ta cũng sẽ triển khai Load Balancer nhằm cân bằng tải và điều phối các yêu cầu truy cập từ phía người dùng đến Application Tier của chúng ta.

Hãy chắc chắn rằng bạn đã xem qua tài liệu Triển khai Ứng dụng FCJ Management trên Máy ảo Windows/AmazonLinux và nắm được cách triển khai ứng dụng trên máy ảo. Chúng ta sẽ cần sử dụng máy ảo được triển khai FCJ Management cho việc triển khai đồng loạt và mở rộng trong Auto Scaling Group.

![ImageArchitecture](/images/1.introduction/000.png?width=50pc)
