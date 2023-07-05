---
title : "Khởi tạo AMI từ Máy ảo"
date :  "`r Sys.Date()`" 
weight : 10
chapter : false
pre : " <b> 2.10 </b> "
---

#### Khởi tạo AMI từ Máy ảo

Ở bước này, bạn sẽ khởi tạo một Amazon Machine Image (AMI) cho Amazon Linux Instance vừa được thiết lập ở bước trước. AMI là một bản chụp cấu hình của EC2 Instance cho phép bạn triển khai nhiều EC2 Instance với cấu hình tương tự với EC2 Instance gốc. AMI thường được sử dụng bên trong Launch Template để tạo khuôn mẫu cho các EC2 Instances.

1. Truy cập vào **EC2**

    - Chọn **Instances**
    - Chọn **FCJ-Management** instance
    - Chọn **Actions**
    - Chọn **Image and templates**
    - Chọn **Create image**

![Deploy app](/images/2.preparation/083-ami.png?width=90pc)

2. Cấu hình **Template**

    - **Image name**, nhập ```FCJ-Management-AMI```
    - **Image description**, nhập ```AMI for FCJ-Management```
    - Chọn **Create image**

![Deploy app](/images/2.preparation/084-ami.png?width=90pc)

3. Quá trình khởi tạo AMI mất khoảng 5 phút. Sau 5 phút, chúng ta thấy **Status** chuyển sang **Available**

![Deploy app](/images/2.preparation/085-ami.png?width=90pc)

Chúng ta đã hoàn thành các bước chuẩn bị cho việc triển khai FCJ Management với Auto Scaling Group.



![Deploy app](/images/2.preparation/086-ami.png?width=90pc)

Ở phần kế tiếp, chúng ta sẽ bắt đầu khởi tạo và triển khai nội dung chính của bài thực hành này.