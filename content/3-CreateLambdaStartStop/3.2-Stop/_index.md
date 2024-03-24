---
title : "Create a Stop instance"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

#### Create a Stop instance

1. Go to **AWS Management Console**

   - Find **Lambda**
   - Select **Lambda**

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0001.png?width=90pc)

2. In the **Lambda** interface

   - Select **Create Function**
  
   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0002.png?width=90pc)

3. Next step

   - Select **Author from scratch**
   - Function name enter **```LambdaEC2Stop```**
   - Runtime select **Python 3.9**
   - Select the arrow **Change default execution role**
   - Select **Use an existing role**
   - Select **LambdaEC2Role**

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0003.png?width=90pc)

   - Scroll down and select **Create function**

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0004.png?width=90pc)

   - Lambda Stop function successfully created

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0005.png?width=90pc)

4. Next step

   - Select **Code**
   - Delete the old code and paste the new code below and edit **Region, Instance**
   - Select Deploy
   - Remember to adjust **Region**. In this article, I am in Region **Singapore** so enter **```ap-southeast-1```**
   - **Instance** Then go to EC2 and copy the ID

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0006.png?width=90pc)

         import boto3
         region = 'ap-southeast-1'
         instances = ['instance Linux ID']
         ec2 = boto3.client('ec2', region_name=region)

         def lambda_handler(event, context):
            ec2.stop_instances(InstanceIds=instances)
            print('stopped your instances: ' + str(instances))
   
   - Successfully deployed

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0007.png?width=90pc)

5. The next step we will try to turn off the instance

   - Select **Test**
   - Select **Create new event**
   - Eventname enter **```EC2Stop```**
   - Select **Private**
   - Select **Save**
   - Select **Test**

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0008.png?width=90pc)

   - Successful notification

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0009.png?width=90pc)

   - Return to EC2 to review the status of the **Stopped** instance

   ![create lambda stop](/images/4-CreateLambda/1LambdaStop/0010.png?width=90pc)
