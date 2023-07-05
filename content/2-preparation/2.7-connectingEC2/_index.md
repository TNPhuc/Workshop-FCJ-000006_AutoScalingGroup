---
title : "Connecting EC2 Instance"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 2.7 </b> "
---

#### Connect EC2 instance
1. Use **MobaXterm** to SSH into the instance via port 22.

    - Select **Session**
![Connect EC2 instance](/images/2.preparation/047-ConnectEC2.png?width=90pc)

2. In the **Session settings** section

    - **Remote host**, enter **Public IPv4 address** of the instance
    - **Specify username**, enter **ec2-user**
    - Check port *22*
    - Select **Advanced SSH settings**
    - Select **Use private key** and select **keypair** of the instance.
    - Select **OK**
![Connect EC2 instance](/images/2.preparation/048-ConnectEC2.png?width=90pc)

3. Follow the instructions in the figure. EC2 instance connection was successful.
![Connect EC2 instance](/images/2.preparation/049-ConnectEC2.png?width=90pc)
![Connect EC2 instance](/images/2.preparation/050-ConnectEC2.png?width=90pc)
![Connect EC2 instance](/images/2.preparation/051-ConnectEC2.png?width=90pc)

4. Install node version manager (nvm) by typing the following in the following command line:

        curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash

![Connect EC2 instance](/images/2.preparation/052-ConnectEC2.png?width=90pc)

5. Enable nvm by typing the following in the command line and Use nvm to install the latest version of Node.js by typing the following in the command line.

        . ~/.nvm/nvm.sh
        nvm install 16

![Connect EC2 instance](/images/2.preparation/053-ConnectEC2.png?width=90pc)

6. Check nodejs is installed successfully

        node -v
        npm -v

![Connect EC2 instance](/images/2.preparation/054-ConnectEC2.png?width=90pc)