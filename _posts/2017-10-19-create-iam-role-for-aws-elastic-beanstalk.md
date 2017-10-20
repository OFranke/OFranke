---
layout: post
title: "Create IAM User Role for AWS Elastic Beanstalk"
date: 19-10-2017
---


Goals for this article:
- Setup a AWS IAM user with Elastic Beanstalk permissions

## 1. Let's start

To create a new IAM user go to [AWS IAM](https://console.aws.amazon.com/iam/home#/home) and in the left
pane, click on "Users". Add a new user via the blue button:
<br>
<br> 
![My helpful screenshot]({{ "/assets/create-iam-role-for-elastic-beanstalk/add_user.jpg" }})


## 2. Set the user details
![set user details]({{ "/assets/create-iam-role-for-elastic-beanstalk/add_user_details.jpg" }})

I think it's in general a good practice to name users according to what they are used for.
The user eb_deployment_application_test stands for: 
>eb: AWS service
<br> 
 deployment: the task the user is doing
<br>
application: the application the user will deploy to elastic beanstalk
<br>
test: the application environment the user will deploy (can be staging, production, etc.)

As we want to use our user to deploy our application to Elastic Beanstalk, the programmatic 
access will be sufficient.


## 3. Define access permissions

The user needs some permissions to access Elastic Beanstalk. I decided to keep it simple for now and 
just give the full access defined by the policy AWSElasticBeanstalkFullAccess. Of course you can also create
user groups and manage all permissions according to your company guidelines.
![set user details]({{ "/assets/create-iam-role-for-elastic-beanstalk/grant_user_permissions.jpg" }})


## 4. Finish user setup

In the next step the user will be created and you can save the credentials somewhere
or download a CSV file. With these credentials you are now able to access Elastic Beanstalk
and use the Elastic Beanstalk Command Line Interface.