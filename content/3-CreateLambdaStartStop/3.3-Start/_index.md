---
title : "Create a Start instance"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

#### Create a Start instance

1. In the **Lambda** interface

   - Select **Create Function**
  
   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0011.png?width=90pc)

2. Next step

   - Select **Author from scratch**
   - Function name enter **```LambdaEC2Start```**
   - Runtime select **Python 3.9**
   - Select the arrow **Change default execution role**
   - Select **Use an existing role**
   - Select **LambdaEC2Role**
   - And scroll down to select **Create function**

   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0012.png?width=90pc)


3. Next step

   - Select **Code**
   - Delete the old code and paste the new code below and edit **Region, Instance**
   - Select Deploy
   - For **Instance**, you can go to EC2 and copy the ID
    {{% notice note %}}
   Remember to adjust **Region**. In this article, I am in Region **Singapore** so enter **```ap-southeast-1```**
    {{% /notice %}}
   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0013.png?width=90pc)


            import boto3
            region = 'ap-southeast-1'
            instances = ['ID instance Linux']
            ec2 = boto3.client('ec2', region_name=region)

            def lambda_handler(event, context):
               ec2.start_instances(InstanceIds=instances)
               print('started your instances: ' + str(instances))
         

4. The next step we will try to turn on the instance

   - Select **Test**
   - Select **Create new event**
   - Eventname enter **```EC2Start```**
   - Select **Private**
   - Select **Save**
   - Select **Test**

   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0014.png?width=90pc)


   - Return to EC2 to review the status of the **Running** instance

   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0015.png?width=90pc)