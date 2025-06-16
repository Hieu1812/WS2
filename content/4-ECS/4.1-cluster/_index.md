+++
title = "Cluster Setup"
date = 2020
weight = 1
chapter = false
pre = "<b>4.1 </b>"
+++

To launch ECS, we need to create a cluster to have resources for container deployment

#### Create cluster

1. Access **ECS**
![cluster](/images/ECS/cluster/1.png)
2. Select Clusters -> Create cluster
![cluster](/images/ECS/cluster/2.png)
3. Enter Cluster name -> select AWS Fargate -> Create 
![cluster](/images/ECS/cluster/3.png)
4. Cluster has been created, now we need to create task definition to create services that will run on the cluster
![cluster](/images/ECS/cluster/4.png)