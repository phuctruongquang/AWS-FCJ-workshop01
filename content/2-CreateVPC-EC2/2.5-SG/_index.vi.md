---
title : "Tạo Security group"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

#### Tạo Security group

1. Trong giao diện **VPC**

   - Chọn **Security groups**
   - Chọn **Create Security group**
  
    ![create SG](/images/2-createVPC/5CreateSG/0001.png?width=90pc)

2. Giao diện **Create security group**

   - Security group name nhập **```SG-start-stop```**
   - Description nhập **```allows ICMP```**
   - VPC Chọn **lambda-start-stop**

 - **Inbound rules**
   - Chọn **Add rule**
   - Type chọn **ALL ICMP- IPv4**
   - Source chọn **0.0.0.0/0**

    ![create SG](/images/2-createVPC/5CreateSG/0002.png?width=90pc)

3. Kéo xuống và chọn **Create security group**
   
    ![create SG](/images/2-createVPC/5CreateSG/0003.png?width=90pc)

4. Tạo thành công

    ![create SG](/images/2-createVPC/5CreateSG/0004.png?width=90pc)