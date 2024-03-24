---
title : "Create Subnet"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

#### Create Subnet

1. In the **VPC** interface

   - Select **Subnets**
   - Select **Create Subnet**
  
   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0001.png?width=90pc)


2. Interface **Create subnet**

   - VPC ID Select **lambda-start-stop**
   - Subnet name enter **```subnet-start-stop```**
   - Availability Zone select **ap-southeast-1a**
   - IPv4 CIDR select **10.0.0.0/16**
   - IPv4 subnet CIDR block enter **```10.0.10.0/24```**
  
   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0002.png?width=90pc)

3. Scroll down and select **Create Subnet**

   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0003.png?width=90pc)

4. **Subnet** has been created successfully

   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0004.png?width=90pc)