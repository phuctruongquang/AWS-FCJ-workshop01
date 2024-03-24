---
title : "Create Policy"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

#### Create Policy

1. Access the **AWS Management Console** interface

   - Find **IAM**
   - Select **IAM**

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0001.png?width=90pc)

2. In the **IAM** interface

   - Select **Policies**
   - Select **Create Policy**

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0002.png?width=90pc)

3. Next step

   - Select **JSON**
   - Delete the old code in **Policy editor** and copy the code below and paste it
   - Select **Next**

               {  "Version": "2012-10-17",
         "Statement": [
            {
               "Effect": "Allow",
               "Action": [
               "logs:CreateLogGroup",
               "logs:CreateLogStream",
               "logs:PutLogEvents"
               ],
               "Resource": "arn:aws:logs:*:*:*"
            },
            {
               "Effect": "Allow",
               "Action": [
               "ec2:Start*",
               "ec2:Stop*"
               ],
               "Resource": "*"
            }
         ]
         }


   

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0003.png?width=90pc)

4. **Policy details**

   - Policy name enter **```LambdaEC2Policy```**
   - Select **Create Policy**

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0004.png?width=90pc)

   - So we have successfully created Policy

#### Next step we will Create Role

1. In the **IAM** interface
   
   - Select **Roles**
   - Select **Create Role**

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0005.png?width=90pc)

2. Next step

   - Select **AWS service**
   - Use case select **Lambda**
   - Select **Next**.

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0006.png?width=90pc)

3. Next step

   - Enter in the search bar we created in the Policies section **```LambdaEC2Policy```**
   - **Check Policy**
   - Select **Next**

   ![alt text](/images/3-CreateIAMPolicy-Role/0007.png?width=90pc)

4. Next step

   - Role name enter  **```LambdaEC2Role```**

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0008.png?width=90pc)

   
   - Select **Create Role**

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0009.png?width=90pc)

5. Successfully created **Role**

   ![create IAM policy](/images/3-CreateIAMPolicy-Role/0010.png?width=90pc)