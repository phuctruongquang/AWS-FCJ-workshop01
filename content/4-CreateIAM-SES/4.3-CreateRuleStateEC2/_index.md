---
title : "Create Rule EventBridge"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

#### Create Rule EventBridge

1. Go to **AWS Management Console**

   - Find **Amazon EventBridge**
   - Select **Amazon EventBridge**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0001.png?width=90pc)

2. In the **Amazon EventBridge** interface

    - Select **Rules**
    - Select **Create rule**
  
    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0002.png?width=90pc)

3. Next **Rule detail**

   - Name enter **```RuleEventBridgeEC2StartStop```**
   - Select **Rule with an event pattern**
   - Select **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0003.png?width=90pc)


4. Next step, scroll down to the **Event pattern** section

   - Event source select **AWS service**
   - AWS service select **EC2**
   - Event type select **EC2 Instance State-change Notification**
   - Event type Specification 1 select **Specific state(s)** press the arrows to select **stopped** and **pending**
   - Event type Specification 2 select **Specific instance id(s)** Specific instance id(s) enter the ID of the Linux instance
   - Next select **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0004.png?width=90pc)

5. Next step

   - Select **Lambda function**
   - Select **LambdaSendMail**
   - Select **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0005.png?width=90pc)

    - Select **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0006.png?width=90pc)

    - Select **Create rule**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0007.png?width=90pc)

    - Rule has been created successfully

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0008.png?width=90pc)