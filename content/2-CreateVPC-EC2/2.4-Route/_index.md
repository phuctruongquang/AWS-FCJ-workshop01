---
title : "Create Route table"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

#### Create Route table

1. In the **VPC** interface

   - Select **Route tables**
   - Select **Create Route table**
  
    ![create route](/aws-fcj-workshop01/images/2-createVPC/4CreateRoute/0001.png?width=90pc)

2. Interface **Route table settings**

   - Enter name **```route-start-stop```**
   - Select **VPC lambda-start-stop**
   - Select **Create route table**

    ![create route](/aws-fcj-workshop01/images/2-createVPC/4CreateRoute/0002.png?width=90pc)

3. Select **Route tables**
   
   - Select **Routes**
   - Select **Edit Routes**
  
    ![create route](/aws-fcj-workshop01/images/2-createVPC/4CreateRoute/0003.png?width=90pc)
  
  

4. Interface **Edit Routes**

 - **Destination section**
   - Select **Add route**
   - Select **0.0.0.0/0**
  
 - **Target section**
   - Select **Internet Gateway**
   - Select **igw-start-stop**
   - Select **Save changes**
  
    ![create route](/aws-fcj-workshop01/images/2-createVPC/4CreateRoute/0004.png?width=90pc)


5. Select **Route tables**

   - Select **Subnet associations**
   - Select **Edit Subnet associations**

    ![create route](/aws-fcj-workshop01/images/2-createVPC/4CreateRoute/0005.png?width=90pc)

   - Select **subnet-start-stop**
   - Select **Save associations**
  
    ![create route](/aws-fcj-workshop01/images/2-createVPC/4CreateRoute/0006.png?width=90pc)