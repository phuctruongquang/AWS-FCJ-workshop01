---
title : "Demo lab"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

### We will create an automatic schedule to turn off the instance

1. Access to **EC2**

    - View the status of the instance which is **Running**

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0001.png?width=90pc)

2. Access to **Amazon EventBridge**

    - Select **ScheduleEC2Stop**
    - Select **Edit**

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0003.png?width=90pc)

3. Next we will fix the time

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0004.png?width=90pc)

    - Select **Next**

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0005.png?width=90pc)

    - Select **Next**

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0006.png?width=90pc)

    - Select **Next**

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0007.png?width=90pc)

    - Select **Save schedule**

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0008.png?width=90pc)

4. Go back to **EC2** and wait until your instance will automatically change its status to **Stopped**

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0009.png?width=90pc)

    {{% notice note %}}
   If the time has come and the instance has not changed its status, please press refresh and wait another 1-3 minutes!
    {{% /notice %}}

    - After the status has been **Stopped** you will receive a notification Email

    ![combine together](/aws-fcj-workshop01/images/7-CombineTogether/0010.png?width=90pc)