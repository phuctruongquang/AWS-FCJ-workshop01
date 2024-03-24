---
title : "Create a Lambda that sends alerts"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

#### Create a Lambda that sends alerts

1. Go to **AWS Management Console**

   - Find **Lambda**
   - Select **Lambda**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0001.png?width=90pc)

2. In the **Lambda** interface

   - Select **Create Function**
  
    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0002.png?width=90pc)

3. Next step

   - Select **Author from scratch**
   - Function name enter **```LambdaEC2SendMail```**
   - Runtime Select **Python 3.9**
   - Select the arrow **Change default execution role**
   - Select **Use an existing role**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0003.png?width=90pc)



    - Scroll down and select role **StateChangeEC2Role**
    - Select **Create function**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0004.png?width=90pc)

4. Next step

   - Select **Code**
   - Delete the old code and paste the new code below and edit the **Email** you verified in **SES**
   - Select Deploy

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0005.png?width=90pc)

            import json
            import boto3

            def lambda_handler(event, context):
                subject = 'Attention Please'
                client = boto3.client("ses")
                body = """
                            <br>
                Your server is changing status: Start/Stop
                    """
                message = {"Subject": {"Data": subject}, "Body": {"Html": {"Data": body}}}
                response = client.send_email(Source = "Enter your email address here", Destination = {"ToAddresses": ["Enter your email address here"]}, Message = message) 
                print("The mail is sent successfully")
   
   - Deployed successfully

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0006.png?width=90pc)

5. The next step is testing

   - Select **Test**
   - Select **Create new event**
   - Eventname enter **```EC2SendMail```**
   - Select **Private**
   - Select **Save**
   - Select **Test**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0007.png?width=90pc)

   - Open **Email** to check. A notification will be sent

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0008.png?width=90pc)