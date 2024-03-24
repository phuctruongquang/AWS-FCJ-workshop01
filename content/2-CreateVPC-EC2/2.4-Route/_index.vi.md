---
title : "Tạo Route table"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

#### Tạo Route table

1. Trong giao diện **VPC**

   - Chọn **Route tables**
   - Chọn **Create Route table**
  
    ![create route](/images/2-createVPC/4CreateRoute/0001.png?width=90pc)

2. Giao diện **Route table settings**

   - Name nhập **```route-start-stop```**
   - Chọn **VPC lambda-start-stop**
   - Chọn **Create route table**

    ![create route](/images/2-createVPC/4CreateRoute/0002.png?width=90pc)

3. Chọn **Route tables**
   
   - Chọn **Routes**
   - Chọn **Edit Routes**
  
    ![create route](/images/2-createVPC/4CreateRoute/0003.png?width=90pc)
  
  

4. Giao diện **Edit Routes**

 - **Phần Destination**
   - Chọn **Add route**
   - Chọn **0.0.0.0/0**
  
 - **Phần Target**
   - Chọn **Internet Gateway**
   - Chọn **igw-start-stop**
 - Chọn **Save changes**
  
    ![create route](/images/2-createVPC/4CreateRoute/0004.png?width=90pc)


5. Chọn **Route tables**

   - Chọn **Subnet associations**
   - Chọn **Edit Subnet associations**

    ![create route](/images/2-createVPC/4CreateRoute/0005.png?width=90pc)

   - Tích chọn **subnet-start-stop**
   - Chọn **Save associations**
  
    ![create route](/images/2-createVPC/4CreateRoute/0006.png?width=90pc)