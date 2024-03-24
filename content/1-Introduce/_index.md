---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Introducing AWS Lambda

   ![introduce lambda](/aws-fcj-workshop01/images/1-introduce/0001-lambda.png?width=30pc)

**AWS Lambda** (temporarily called Lambda) is a serverless computing service, based on the FaaS (Function-as-a-service) model. When using this service, users will not need to care about the underlying system infrastructure. Lambda will execute user-specified code when required. This helps users, especially programmers, have more time to focus on developing their applications.

Programming languages currently supported include:
- Java
- Python
- C#
- Node.js
- Go
- PowerShell
- Ruby

Users use the above supported programming languages to create Lambda functions. These functions will be charged based on the processing time (duration time) corresponding to the memory capacity of the function. And each function creation area will have different fees, see the cost reference for each area here [AWS Lambda Pricing](https://aws.amazon.com/lambda/pricing/) 

#### Introducing Amazon EventBridge

   ![introduce EventBridge](/aws-fcj-workshop01/images/1-introduce/0002-eventbridge.png?width=30pc)

**Amazon EventBridge** is a service that allows you to build applications that react to events quickly, easily, and securely. EventBridge provides a decentralized event bus that allows you to transfer events between applications, services, and AWS resources.

**Benefits of Amazon EventBridge:**

- Ease of use: EventBridge provides a simple interface for creating, sending, and receiving events.

- Scalability: EventBridge can handle millions of events per second.

- Security: EventBridge provides enterprise-level security.

- Integration: EventBridge integrates with over 200 popular AWS services and SaaS applications.

**Some common use cases for Amazon EventBridge:**

- Automate tasks: EventBridge can be used to automate tasks such as data transformation, data analysis, and process management.

- Build event-driven applications: EventBridge can be used to build event-driven applications such as data streams, alert systems, and IoT applications.

- Connect AWS services: EventBridge can be used to connect AWS services together, making it easy to build complex application architectures.

#### Introducing Amazon Simple Email Service

   ![introduce SES](/aws-fcj-workshop01/images/1-introduce/0003-SES.png?width=30pc)

**Amazon Simple Email Service (SES)** is a cost-effective, high-volume email sending service built on reliable, scalable infrastructure released by Amazon. With Amazon SES, you can use a variety of solutions: send transactional emails, marketing messages, test autoresponders, or anything else.

Currently, Amazon SES has two pricing models: One for receiving emails (which is the heart of this service) and two for sending emails.

The cost of receiving Amazon SES emails depends on two factors: The number of emails and the size of the emails you receive.

The cost of sending Amazon SES emails depends on two factors: The number of emails, the size of the emails, and the size of the attachments you send.

For example: If the email you receive is under **256KB and has no attachments**, receiving the email is free. Additionally, Amazon SES has a limit of 1,000 monthly emails for the free tier of the service.

See cost information here [Amazon SES pricing](https://aws.amazon.com/ses/pricing/)