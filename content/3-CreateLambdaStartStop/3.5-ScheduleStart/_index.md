---
title : "Create a schedule to automatically turn on instances"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 3.5 </b> "
---

#### Create a schedule to automatically turn on instances

1. In the **Amazon EventBridge** interface

   - Select **Schedules**
   - Select **Create Schedule**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0001.png?width=90pc)

2. In **Specify schedule detail**

   - Schedule name enter **```ScheduleEC2Start```**
   - Select **Recurring schedule**
   - Select **(UTC+07:00) Asia/BangKok**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0002.png?width=90pc)

3. Next step

   - Select **Cron-based schelude**
   - In the **Cron experssion** section, we will enter the actual time you want Instance to Start. Refer to [Schedule types on EventBridge Scheduler](https://docs.aws.amazon.com/scheduler/latest/UserGuide/schedule-types.html?icmpid=docs_console_unmapped)

   - Select **OFF**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0003.png?width=90pc)

   - **Minutes** -> Enter the minute you want to shut down the instance
   - **Hours** -> Enter the hour you want to turn off the instance
   - **Day of moth** -> Enter ? will run every day of the month
   - **Month** -> Enter * will run all months of the year
   - **Day of the week** -> If you enter Mon-Sat, it will run from Monday to Saturday
   - **Year** -> Entering * will get the year according to the current milestone
   
   - Scroll down and select **Next**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0004.png?width=90pc)


4. Next step

   - Select **Templated targets**
   - Select **AWS Lambda Invoke**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0005.png?width=90pc)

5. Scroll down below
   - **Invoke** section
   - **Lambda function** enter **```LambdaEC2Start```**
   - Add the following code to the **Payload** section
   - Select **Next**

         {
            "action": "start"
         }
            
   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0006.png?width=90pc)

6. Go ahead and scroll down to the bottom of the page

   - **Role name** enter **```Amazon_EventBridge_Scheduler_LAMBDA_StartEC2```**
   
   - Select **Next**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0007.png?width=90pc)

   {{% notice note %}}
   In this Role name section will be created and located at [CloudWatch](https://us-east-1.console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups) Log group, you can see more
   {{% /notice %}}

   - Scroll down and select **Create schedule**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0008.png?width=90pc)

   - The automatic calendar has been created successfully

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0009.png?width=90pc)

   - You wait until the previously set time, and return to EC2 to check the instance
   - Instance status is **Pending**

   ![create EventBridge Start](/images/4-CreateLambda/4CreateEventBridgeStart/0010.png?width=90pc)

   {{% notice note %}}
   If the time has come and the instance has not changed its status, please press refresh and wait another 1-3 minutes!
   {{% /notice %}}