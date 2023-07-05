---
title : "Khởi tạo Auto Scaling Group"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

#### Khởi tạo Auto Scaling Group

Ở phần này, chúng ta sẽ triển khai một Auto Scaling Group cho ứng dụng FCJ Management để đảm bảo ứng dụng của chúng ta sẽ được triển khai với tính sẵn sàng cao, và có khả năng tăng số lượng EC2 instance khi người dùng truy cập vào hệ thống tăng.

1. Truy cập vào **EC2**

    - Chọn **Auto Scaling Groups**
    - Chọn **Create Auto Scaling group**

![Auto Scaling Group](/images/6.asg/0001.png?width=90pc)

2. **Auto Scaling Group name**, nhập```FCJ-Management-ASG```
![Auto Scaling Group](/images/6.asg/0002.png?width=90pc)

3. Cấu hình template

    - **Launch template** chọn **FCJ-Management-template**
    - chọn **Next**

![Auto Scaling Group](/images/6.asg/0003.png?width=90pc)

4. Tiến hành cấu hình **Network**

    - Chọn **VPC** đã tạo.
    - Chọn **AZ and subnet**

![Auto Scaling Group](/images/6.asg/0004.png?width=90pc)

5. Chọn **Next**

![Auto Scaling Group](/images/6.asg/0005.png?width=90pc)

6. Tiến hành cấu hình **Load balancing**

    - Chọn **Attach to an existing load balancer**
    - Chọn **Choose from your load balancer target groups**
    - Chọn **FCJ-Management-TG**

![Auto Scaling Group](/images/6.asg/0006.png?width=90pc)

7. Chọn **Next**

![Auto Scaling Group](/images/6.asg/0007.png?width=90pc)

8. Thực hiện cấu hình group size vè scaling policy.

    - Desired capacity: Nhập 1. (Default)
    - Minimum capacity: Nhập 1. (Default)
    - Maximum capacity: Nhập 3.

![Auto Scaling Group](/images/6.asg/0008.png?width=90pc)

9. Tại mục **Scaling policies** - optional: Lựa chọn trong bài thực hành này nhằm tạo điều kiện dễ dàng hơn cho bước kiểm tra được thực hiện tiếp theo. Bạn hoàn toàn có thể thiết lập chính sách scale tài nguyên theo nhu cầu của bạn.

    - Chọn **Target tracking scaling policy**
    - **Scaling policy name**, Nhập ```Target Tracking Policy```
    - **Metric type**, chọn **Application Load Balancer request count per target**
    - **Target group**, chọn ```FCJ-Management```
    - **Target value**, nhập 30

![Auto Scaling Group](/images/6.asg/0009.png?width=90pc)

10. Chọn **Next**

![Auto Scaling Group](/images/6.asg/00010.png?width=90pc)

11. Chọn **Create a topic**

![Auto Scaling Group](/images/6.asg/00011.png?width=90pc)

12. Cấu hình **Add notifications**. Chọn **Next**

![Auto Scaling Group](/images/6.asg/00012.png?width=90pc)

- Kiểm tra email và **Confirm subscription**

![Auto Scaling Group](/images/6.asg/00013.png?width=90pc)
![Auto Scaling Group](/images/6.asg/00014.png?width=90pc)

13. Chọn **Create Auto Scaling group**

![Auto Scaling Group](/images/6.asg/00015.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00016.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00017.png?width=90pc)

14. Hoàn thành tạo **Auto Scaling groups**

![Auto Scaling Group](/images/6.asg/00018.png?width=90pc)

15. Quá trình khởi tạo Auto Scaling Group sẽ được thực hiện, Auto Scaling Group vừa được tạo sẽ hiển thị trong danh sách, và bạn có thể chọn vào nó để xem thông tin chi tiết.

    - Chúng ta có thể theo dõi các EC2 instance hiện có trong Auto Scaling Group ở trang **Instance management**. Các instance có tình trạng InService là các instance đã sẵn sàng hoạt động.

![Auto Scaling Group](/images/6.asg/00019.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00020.png?width=90pc)

![Auto Scaling Group](/images/6.asg/00021.png?width=90pc)