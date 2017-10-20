---
layout: post
title: "Deploy Laravel App to AWS Elastic Beanstalk via Bitbucket Pipeline"
date: 19-10-2017
---

In this article you will learn:
- how to setup Bitbucket Pipelines
- how to setup a Laravel Application on AWS Elastic Beanstalk
- how to manage different environments (staging, production) on AWS Elastic Beanstalk
- how to enable auto deployment for different branches to your environments

## Let's start

Given that you already registered on Bitbucket and imported your Laravel project, 
go to your repository and enable pipelines. 
>Bitbucket uses a ***bitbucket-pipelines.yml*** that triggers the build process
>Choose the PHP template and commit it to your repository. See that the first 
build is triggered. We will go into the configuration details in a later step.

## Now Setup AWS Elastic Beanstalk
test
## Create an IAM user for you deployment
see the details in this article here: [Create IAM role for AWS Elastic Beanstalk](create-iam-role-for-aws-elastic-beanstalk)

# some codeblock
```php
$test = 'text';
```
## More content will follow



## Sources:
- https://deliciousbrains.com/scaling-laravel-using-aws-elastic-beanstalk-part-3-setting-elastic-beanstalk/
- https://stackoverflow.com/questions/43849436/create-multiple-pipelines-for-one-repository-on-bitbucket
- https://www.dowebthings.com/how-to-deploy-from-gitlab-to-elastic-beanstalk-aws/

