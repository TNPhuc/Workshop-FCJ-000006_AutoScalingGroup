---
title : "Khởi tạo Target Group"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### Khởi tạo Target Group

1. Truy cập giao diện **EC2**

    - Chọn **Target Groups**
    - Chọn **Create target group**

![Deploy app](/images/4.createtg/001-tg.png?width=90pc)

2. Thực hiện cấu hình

    - Chọn **Instances**

![Deploy app](/images/4.createtg/002-tg.png?width=90pc)

3. Ở trang **Specify group details**,  thiết lập các thông số như sau cho **target group:**

    - **Target group name:** E Nhập tên của target group (VD: ```FCJ-Management-TG```).
    - **Protocol**: *HTTP*.
    - **Port: 5000** (Port sử dụng bởi FCJ Management).
    - Các mục còn lại để mặc định.

![Deploy app](/images/4.createtg/003-tg.png?width=90pc)

4. Chọn **Next**

![Deploy app](/images/4.createtg/004-tg.png?width=90pc)

5. Trong giao diện **Available instances**

    - Chọn **FCJ-Management** instance
    - Chọn port **5000**
    - Chọn **Include as pending below** ( nếu không chọn lúc truy cập bằng DNS Load Balancer sẽ gặp lỗi **HTTP 503: Service unavailable**)
    - Kiểm tra lại
    - Chọn **Create target group**

![Deploy app](/images/4.createtg/005-tg.png?width=90pc)

6.  Trong giao diện **Register pending targets only**, chọn **Continue**

![Deploy app](/images/4.createtg/006-tg.png?width=90pc)

7. Hoàn thành tạo **Target group**

![Deploy app](/images/4.createtg/007-tg.png?width=90pc)