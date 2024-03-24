---
title : "Create Security group"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

#### Create Security group

1. In the **VPC** interface

   - Select **Security groups**
   - Select **Create Security group**
  
    ![create SG](/images/2-createVPC/5CreateSG/0001.png?width=90pc)

2. Interface **Create security group**

   - Security group name enter **```SG-start-stop```**
   - Description enter **```allows ICMP```**
   - VPC Select **lambda-start-stop**

 - **Inbound rules**
   - Select **Add rule**
   - Type Select **ALL ICMP- IPv4**
   - Source Select **0.0.0.0/0**

    ![create SG](/images/2-createVPC/5CreateSG/0002.png?width=90pc)

3. Scroll down and select **Create security group**
   
    ![create SG](/images/2-createVPC/5CreateSG/0003.png?width=90pc)

4. Created successfully

    ![create SG](/images/2-createVPC/5CreateSG/0004.png?width=90pc)