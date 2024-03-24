---
title : "Verify email to SES"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 2.7 </b> "
---

#### Verify email to SES

1. Go to **AWS Management Console**

   - Find **SES**
   - Select **Amazon Simple Email Service**

    ![SES](/images/2-createVPC/7CreateSES/0001.png?width=90pc)


2. In the **Amazon SES** interface

   - Select **Identities**
   - Select **Create indentity**

    ![SES](/images/2-createVPC/7CreateSES/0002.png?width=90pc)

3. **Identity details**
   
   - Select **Email address**
   - In the Email address section, enter your email
   - Select **Create identity**

    ![SES](/images/2-createVPC/7CreateSES/0003.png?width=90pc)

4. Notification waiting for verification **email**

    ![SES](/images/2-createVPC/7CreateSES/0004.png?width=90pc)

5. Open your email and you will see an email from Amazon Web Service sent to you

    - Click on the link
    
    ![SES](/images/2-createVPC/7CreateSES/0005.png?width=90pc)

6. Verification was successful

    ![SES](/images/2-createVPC/7CreateSES/0006.png?width=90pc)

    - Go back and check

    ![SES](/images/2-createVPC/7CreateSES/0007.png?width=90pc)