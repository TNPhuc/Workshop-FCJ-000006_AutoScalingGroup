---
title : "Tạo DB Subnet Group"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

#### Tạo DB Subnet Group
1. Truy cập vào [RDS](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1)

    - Chọn **Subnet groups**
    - Chọn **Create DB subnet group**
![Create SG](/images/2.preparation/019-CreateDBSG.png?width=90pc)

2. Trong giao diện **Create DB subnet group**

    - **Name**, nhập ```FCJ-Management-Subnet-Group```
    - **Description**, nhập ```Subnet Group for FCJ Management```
    - Chọn VPC đã tạo.
![Create SG](/images/2.preparation/020-CreateDBSG.png?width=50pc)

3. Tiến hành cấu hình **subnet**

    - Chọn các **AZ**
    - Chọn **subnet**
    - Chọn **Create**
![Create SG](/images/2.preparation/021-CreateDBSG.png?width=50pc)

4. Thành công tạo **DB Subnet Group**
![Create SG](/images/2.preparation/022-CreateDBSG.png?width=50pc)
![Create SG](/images/2.preparation/023-CreateDBSG.png?width=50pc)