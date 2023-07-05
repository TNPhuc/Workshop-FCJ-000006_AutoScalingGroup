---
title : "Create DB instance"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

#### Create DB instance
1. Go to **AWS Management Console**

    - Find **RDS**
    - Select **RDS**
![Create DB instance](/images/2.preparation/024-CreateDB.png?width=90pc)

2. In **RDS** interface

    - Select **Databases**
    - Select **Create database**
![Create DB instance](/images/2.preparation/025-CreateDB.png?width=90pc)

3. Choose the method to create **database**

    - Select **Standard create**
![Create DB instance](/images/2.preparation/026-CreateDB.png?width=90pc)

4. Configure **Engine** database

    - Select **MySQL**
![Create DB instance](/images/2.preparation/027-CreateDB.png?width=90pc)

5. Configure **Template**

    - Select **Dev/Test**
    - For **Availability and durability**, select **Mutil-AZ DB instance**
![Create DB instance](/images/2.preparation/028-CreateDB.png?width=90pc)

6. Next, make detailed settings

    - **DB instance identifier**, enter ```fcj-management-db-instance```
    - **Master user**, enter **admin**
    - **Master password**, enter your choice (in the lab, enter ```phuc2002```)
    - **Confirm password**, enter the password again.
![Create DB instance](/images/2.preparation/029-CreateDB.png?width=90pc)

7. Perform network configuration for db instance

    - **Network type**, select **IPv4**
    - **VPC**, select **asg-vpc** created
    - **Subnet group**, select the created subnet group.
    - **VPC security group**, Select **Choose existing**
    - **Security Group**, select **FCJ-Management-DB-SG** (to avoid confusion with web SG).
![Create DB instance](/images/2.preparation/030-CreateDB.png?width=90pc)

8. Initialize Database with the name **awsuser**, leave the rest to default.
![Create DB instance](/images/2.preparation/031-CreateDB.png?width=90pc)

    - Lưu ý: Ở tùy chọn Deletion protection, giá trị mặc định là Enable giúp bảo vệ cơ sở dữ liệu khỏi bị vô tình xóa (Protects the database from being deleted accidentally). Tuy nhiên, trong bài lab này, ta Disable Deletion protection để dễ dọn dẹp tài nguyên vào cuối bài lab.
9. Check again and select **Create database**
![Create DB instance](/images/2.preparation/032-CreateDB.png?width=90pc)

10. Initialize DB instance in 10 minutes. When **Status** changes to **Available**, it’s done.

    - Select **db instance** just created.
![Create DB instance](/images/2.preparation/033-CreateDB.png?width=90pc)

11. In the **Connectivity & security** interface

    - Store value **Endpoint**
    - Check **port** *3306*
![Create DB instance](/images/2.preparation/034-CreateDB.png?width=90pc)
![Create DB instance](/images/2.preparation/035-CreateDB.png?width=90pc)