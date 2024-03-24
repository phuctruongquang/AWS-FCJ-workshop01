---
title : "Create Role"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

#### Create Role

1. Go to **AWS Management Console**

   - Find **IAM**
   - Select **IAM**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0001.png?width=90pc)

2. In the **IAM** interface

   - Select **Roles**
   - Select **Create role**
  
    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0002.png?width=90pc)

3. Next step

   - Select **AWS service**
   - **Use case** Select **Lambda**
   - Select **Next**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0003.png?width=90pc)


4. Next step

   - Type in the search bar **```CloudWatchFullAccess```**
   - **Select CloudWatchFullAccess**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0004.png?width=90pc)

    - Type in the search bar **```AmazonSESFullAccess```**
    - **Select AmazonSESFullAccess**
    - Select **Next**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0005.png?width=90pc)

5. Next step

   - Role name enter  **```StateChangeEC2Role```**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0006.png?width=90pc)


   - Scroll down below and select **Create Role**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0007.png?width=90pc)

6. Successfully created **Role**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0008.png?width=90pc)