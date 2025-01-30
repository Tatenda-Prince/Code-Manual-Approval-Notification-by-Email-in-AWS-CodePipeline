# Code-Manual-Approval-Notification-by-Email-in-AWS-CodePipeline

"Pipeline Notifications"

![image_alt](https://github.com/Tatenda-Prince/Code-Manual-Approval-Notification-by-Email-in-AWS-CodePipeline/blob/4d47aa1116c72fb1aff85cde42ef008630f9e133/img/Screenshot%202025-01-29%20205145.png) 

## Introduction 

DevOps teams employ the Continuous Integration and Continuous Delivery (CI/CD) process to deliver code updates more regularly and consistently. CI/CD is a great practice for devops teams. Additionally, it is an agile methodology best practice. Software development teams can concentrate on fulfilling business needs while maintaining code quality and software security by automating integration and delivery with CI/CD.

It's normal to forget to implement code changes in the realm of rapid software development. Adding an email notification system for code approval can be a game-changer to address this. We'll show you how to use AWS CodePipeline and Simple Notification Service (SNS) to set up email notifications for code approvals in this small project.

## Prerequisites

Before diving into the steps, make sure you have the following prerequisites in place:

1.AWS CodePipeline configured for your project.

2.AWS Beanstalk platform set up for code deployment.

3.Simple Notification Service (SNS) for sending email notifications.

## Manual Approval Approach

We follow the manual approval process, which necessitates human involvement prior to code deployment. This procedure adds an additional degree of security by guaranteeing that only authorised users can deploy the code.


## Step 1: Configure Simple Notification Service (SNS)

Streamlining Notifications with SNS

The first step is to establish an SNS topic that will act as the bridge between your CodePipeline and email notifications. Head over to the AWS SNS console, create a topic, and configure email subscriptions. Once confirmed, you’re ready to receive notifications about your pipeline directly in your inbox.

1.1.Login to AWS Console:

Access the AWS Management Console and search for Simple Notification Service (SNS).

1.2.Create Topic

In SNS, create a new topic with a meaningful name.

Choose “Create topic.

![image_alt](https://github.com/Tatenda-Prince/Code-Manual-Approval-Notification-by-Email-in-AWS-CodePipeline/blob/484f5895dfe3db0bb221e86e7d3ac1befe31ff04/img/Screenshot%202025-01-30%20151105.png)


Give your topic a name

![image_alt]()


proceed and click create


1.3.After creating the topic, click on it.

Add a subscription with the following details:

![image_alt]()



Topic Arn: Choose the recently created topic.

Protocol: Select “Email.”

Endpoint: Enter the email address where you want to receive the approval link.

![image_alt]()


Click “Create Subscription.”


Make sure you confirm  subscription from your own email to see example below-


![image_alt]()






