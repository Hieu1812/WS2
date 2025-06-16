+++
title = "Developing CI/CD for Backend using Docker with AWS Services"
date = 2024
weight = 1
chapter = false
+++

# Developing CI/CD for Backend using Docker with AWS Services

### Overview

In this lab, you will learn about AWS services in implementing CI/CD pipeline.

![ConnectPrivate](/images/WS2.png)

### ECR
- A docker image registry service provided by Amazon Web Services (AWS). Using ECR can integrate with other services like ECS, EKS, etc. more conveniently with high availability.

### CodePipeline
- An AWS service that helps us build pipeline flow for CI/CD. In this article, there will be 3 stages: Source, Build, Deploy. Source will be triggered via push command in the configured github repo. Build will trigger CodeBuild, Deploy will trigger CodeDeploy.

### CodeBuild
- CodeBuild will perform the role of building source code so that the application can be ready to deploy. It will execute build commands through a yaml config file containing all build commands and related configurations.

### ECS
- A fully managed container orchestration service that will help deploy, manage and scale packaged applications more efficiently. In this article, we will use the serverless structure Fargate.

### ALB
- Application Load Balancer is load balancing at the application layer (Layer 7 - HTTP). Helps coordinate HTTP Requests to different service servers (target groups) or applications on the same server.

### Contents

1. [Setup and push image to ECR](1-SetupECR/)
2. [VPC Setup](2-VPC/)
3. [CodeBuild Setup](3-CodeBuild/)
4. [ECS Setup and Launch](4-ECS/)
5. [CodePipeline Setup](5-Portfwd/)
6. [Resource Cleanup](6-cleanup/)

