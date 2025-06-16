+++
title = "Service Setup"
date = 2020
weight = 1
chapter = false
pre = "<b>4.3 </b>"
+++

To launch ECS, we need to create a cluster to have resources for container deployment

#### Create service

1. Access cluster in **ECS**, select Service and Create
![cluster](/images/ECS/service/1.png)
2. On the create service page:
    - Select task definition, the latest version of task df will be automatically selected.
    - In environment, we'll select launch type with fargate and the latest platform version.
    ![cluster](/images/ECS/service/2.png)
    - Desired tasks will be selected based on needs. The number of tasks will be launched based on preset parameters.
    - Choose the same VPC as selected in task definition. Select appropriate subnets (here we choose 2 public subnets)
    ![cluster](/images/ECS/service/3.png)
    - Select the security group created in Page 2
    - Since our project uses Load balancing, we'll check to use with port 80 and HTTP method
    ![cluster](/images/ECS/service/4.png)
    - Name the load balancer and target group, then review and select Create
    ![cluster](/images/ECS/service/5.png)
3. Access load balancer to get DNS access. 
    - when accessing the page, we can see the IP address of the running container. After reloading the page, it will change to a new IP address from another container
    ![cluster](/images/ECS/service/6.png)
    ![cluster](/images/ECS/service/7.png)

{{%notice tip%}}
You can adjust the load balancing algorithm in **Edit target group attributes** in the created target group.
Enable stickiness to link and maintain sessions between client and container
{{%/notice%}}

