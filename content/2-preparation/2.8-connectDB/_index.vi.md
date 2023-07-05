---
title : "Kết nối DB Instance"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 2.8 </b> "
---

#### Kết nối DB instance
1. Sử dụng quyền **user root**

        sudo su

![Connect DB instance](/images/2.preparation/055-ConnectDB.png?width=90pc)

2. Cài đặt *MySQL* command-line client

        yum install mariadb

![Connect DB instance](/images/2.preparation/056-ConnectDB.png?width=90pc)
![Connect DB instance](/images/2.preparation/057-ConnectDB.png?width=90pc)

3. Kiểm tra cài đặt thành công

        mysql --version

![Connect DB instance](/images/2.preparation/058-ConnectDB.png?width=90pc)

4. Kết nối từ *MySQL* command-line client (unencrypted)

    - Đối với tham số -h, hãy thay thế DNS name (endpoint) cho DB instance
    - Đối với tham số -P, hãy thay thế cổng cho DB instance. (3306)
    - Đối với tham số -u, thay bằng master user
    - Nhập master user password
    
            mysql -h db-instance.crmmitoajvxx.us-east-1.rds.amazonaws.com -P 3306 -u admin -p

![Connect DB instance](/images/2.preparation/059-ConnectDB.png?width=90pc)
![Connect DB instance](/images/2.preparation/060-ConnectDB.png?width=90pc)
![Connect DB instance](/images/2.preparation/061-ConnectDB.png?width=90pc)

5. Kết nối DB instance thành công. Tiến hành kiểm tra các database trong instance bằng lệnh sẽ in ra danh sách tất cả các cơ sở dữ liệu.

        SHOW DATABASES;
![Connect DB instance](/images/2.preparation/062-ConnectDB.png?width=90pc)

6. Chọn cơ sở dữ liệu để thực hiện các thay đổi đối với nó bằng cách sử dụng USE.

        USE <created database>;
![Connect DB instance](/images/2.preparation/063-ConnectDB.png?width=90pc)

7. Thực hiện tạo bảng trong database awsuser bằng lệnh CREATE TABLE.

        CREATE TABLE `awsfcjuser`.`user` ( `id` INT NOT NULL AUTO_INCREMENT , `first_name` VARCHAR(45) NOT NULL , `last_name` VARCHAR(45) NOT NULL , `email` VARCHAR(45) NOT NULL , `phone` VARCHAR(45) NOT NULL , `comments` TEXT NOT NULL , `status` VARCHAR(10) NOT NULL DEFAULT 'active' , PRIMARY KEY (`id`)) ENGINE = InnoDB;
![Connect DB instance](/images/2.preparation/064-ConnectDB.png?width=90pc)

8. VXác minh rằng bảng được tạo bằng lệnh **DESCRIBE**

        DESCRIBE user;
![Connect DB instance](/images/2.preparation/065-ConnectDB.png?width=90pc)

9. Chèn thông tin vào trong bảng dữ liệu bằng lệnh **INSERT INTO**

        INSERT INTO `user` 
        (`id`, `first_name`,  `last_name`,    `email`,                 `phone`,         `comments`, `status`) VALUES
        (NULL, 'Amanda',      'Nunes',        'anunes@ufc.com',        '012345 678910', '',          'active'),
        (NULL, 'Alexander',   'Volkanovski',  'avolkanovski@ufc.com',  '012345 678910', '',          'active'),
        (NULL, 'Khabib',      'Nurmagomedov', 'knurmagomedov@ufc.com', '012345 678910', '',          'active'),
        (NULL, 'Kamaru',      'Usman',        'kusman@ufc.com',        '012345 678910', '',          'active'),
        (NULL, 'Israel',      'Adesanya',     'iadesanya@ufc.com',     '012345 678910', '',          'active'),
        (NULL, 'Henry',       'Cejudo',       'hcejudo@ufc.com',       '012345 678910', '',          'active'),
        (NULL, 'Valentina',   'Shevchenko',   'vshevchenko@ufc.com',   '012345 678910', '',          'active'),
        (NULL, 'Tyron',       'Woodley',      'twoodley@ufc.com',      '012345 678910', '',          'active'),
        (NULL, 'Rose',        'Namajunas ',   'rnamajunas@ufc.com',    '012345 678910', '',          'active'),
        (NULL, 'Tony',        'Ferguson ',    'tferguson@ufc.com',     '012345 678910', '',          'active'),
        (NULL, 'Jorge',       'Masvidal ',    'jmasvidal@ufc.com',     '012345 678910', '',          'active'),
        (NULL, 'Nate',        'Diaz ',        'ndiaz@ufc.com',         '012345 678910', '',          'active'),
        (NULL, 'Conor',       'McGregor ',    'cmcGregor@ufc.com',     '012345 678910', '',          'active'),
        (NULL, 'Cris',        'Cyborg ',      'ccyborg@ufc.com',       '012345 678910', '',          'active'),
        (NULL, 'Tecia',       'Torres ',      'ttorres@ufc.com',       '012345 678910', '',          'active'),
        (NULL, 'Ronda',       'Rousey ',      'rrousey@ufc.com',       '012345 678910', '',          'active'),
        (NULL, 'Holly',       'Holm ',        'hholm@ufc.com',         '012345 678910', '',          'active'),
        (NULL, 'Joanna',      'Jedrzejczyk ', 'jjedrzejczyk@ufc.com',  '012345 678910', '',          'active');
![Connect DB instance](/images/2.preparation/066-ConnectDB.png?width=90pc)

10. Sử dụng lệnh **SELECT** để hiển thị bảng:

        SELECT * FROM user;
![Connect DB instance](/images/2.preparation/067-ConnectDB.png?width=90pc)

11. Sử dụng **exit** đề rời khỏi. Nếu không thể ngắt kết nối với DB instance, hãy dùng tổ hợp phím *Ctrl+C*
![Connect DB instance](/images/2.preparation/068-ConnectDB.png?width=90pc)