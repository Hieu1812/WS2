+++
title = "VPC Configuration"
date = 2020
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

In this section, you will set up VPC and security groups for the clusters
### VPC Setup
<!-- {{% notice info %}}
{{% /notice %}} -->
1. Access **VPC**.
!["VPC"](/images/VPC/6.png)
2. Select **Create VPC**.
!["VPC"](/images/VPC/7.png)
3. Choose VPC and more to set up subnets simultaneously
4. Enter the required information in sections 2 and 3, select the number of AZs needed. In this workshop, we will use ALB so we need to select 2 or more AZs
!["VPC"](/images/VPC/1.png)
5. Choose the number of Public subnets and Private Subnets. Then click create to complete the VPC setup
!["VPC"](/images/VPC/2.png)
6. After setup, go to VPC -> select the subnet you will use
!["VPC"](/images/VPC/3.png)
7. Choose actions -> Edit subnet settings
!["VPC"](/images/VPC/4.png)
8. Check Enable auto-assign public ipv4 address and save. Continue doing this with other subnets you will use
!["VPC"](/images/VPC/5.png)


