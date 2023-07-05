---
title : "Connecting DB Instance"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 2.8 </b> "
---

#### Connect DB instance
1. Use **user root** privileges

        sudo su

![Connect DB instance](/images/2.preparation/055-ConnectDB.png?width=90pc)

2. Install *MySQL* command-line client

        yum install mariadb

![Connect DB instance](/images/2.preparation/056-ConnectDB.png?width=90pc)
![Connect DB instance](/images/2.preparation/057-ConnectDB.png?width=90pc)

3. Check the installation is successful

        mysql --version

![Connect DB instance](/images/2.preparation/058-ConnectDB.png?width=90pc)

4. Connect from *MySQL* command-line client (unencrypted)

    - For the -h parameter, replace the DNS name (endpoint) for the DB instance
    - For the -P parameter, substitute the port for the DB instance. (3306)
    - For the -u parameter, replace it with master user
    - Enter master user password
    
            mysql -h db-instance.crmmitoajvxx.us-east-1.rds.amazonaws.com -P 3306 -u admin -p

![Connect DB instance](/images/2.preparation/059-ConnectDB.png?width=90pc)
![Connect DB instance](/images/2.preparation/060-ConnectDB.png?width=90pc)
![Connect DB instance](/images/2.preparation/061-ConnectDB.png?width=90pc)

5. DB instance connection successful. Check the databases in the instance with the command that will print out a list of all the databases.

        SHOW DATABASES;
![Connect DB instance](/images/2.preparation/062-ConnectDB.png?width=90pc)

6. Select the database to make changes to using USE.

        USE <created database>;
![Connect DB instance](/images/2.preparation/063-ConnectDB.png?width=90pc)

7. Create a table in the awsuser database with the CREATE TABLE command.

        CREATE TABLE `awsfcjuser`.`user` ( `id` INT NOT NULL AUTO_INCREMENT , `first_name` VARCHAR(45) NOT NULL , `last_name` VARCHAR(45) NOT NULL , `email` VARCHAR(45) NOT NULL , `phone` VARCHAR(45) NOT NULL , `comments` TEXT NOT NULL , `status` VARCHAR(10) NOT NULL DEFAULT 'active' , PRIMARY KEY (`id`)) ENGINE = InnoDB;
![Connect DB instance](/images/2.preparation/064-ConnectDB.png?width=90pc)

8. Verify that the table is created with the *DESCRIBE* command

        DESCRIBE user;
![Connect DB instance](/images/2.preparation/065-ConnectDB.png?width=90pc)

9. Insert information into the data table with the *INSERT INTO* command

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

10. Use the *SELECT* command to display the table:

        SELECT * FROM user;
![Connect DB instance](/images/2.preparation/067-ConnectDB.png?width=90pc)

11. Use **exit** to leave. Add If cannot disconnect from DB instance, use *Ctrl+C*
![Connect DB instance](/images/2.preparation/068-ConnectDB.png?width=90pc)