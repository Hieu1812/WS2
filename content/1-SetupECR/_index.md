+++
title = "Config and push image to ECR"
date = 2020
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

In this section, you will create a private repository to store software image files
### Creating ECR
1. Access **ECR**.
![ECR](/images/ECR/1.png)
2. In the left navigation bar, select **Private repositories**.
3. Click **Create repositories**.
![ECR](/images/ECR/2.png)
4. Enter the repository name. It's recommended to use the same name as the tag used when building docker for better management, then click create.
5. If you have never used AWS CLI before, from this step we will guide you through installing and creating an IAM user for CLI.
6. Download AWS CLI from the following link [AWS CLI](URL "https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html") and install as normal
7. Create a user to log in to CLI. Within the scope of this workshop, we will only add basic permissions to push images to ECR. Access **IAM**
![ECR](/images/ECR/6.png)
8. Select User => create user
![ECR](/images/ECR/7.png)
9. Enter the username.
![ECR](/images/ECR/8.png)
10. Select Attach policies directly => search for and select **AmazonEC2ContainerRegistryPowerUser** => next
![ECR](/images/ECR/9.png)
11. Click create. The new account will be created immediately, access the account details => create access key.
![ECR](/images/ECR/10.png)
12. We will be using this in the CLI scope so select CLI => check agree => next
![ECR](/images/ECR/11.png)
13. We will skip this step to create the access key directly
![ECR](/images/ECR/12.png)
14. The access key has been created successfully. You should download it as a CSV file to be able to view it more easily as it can only be viewed and downloaded once.
![ECR](/images/ECR/13.png)
15. Then access the cmd and type ```aws configure``` and log in using the key downloaded in the previous step along with the region.
16. Now we can use AWS's built-in commands in the IDE
![ECR](/images/ECR/4.png)
17. After performing the available steps, the built image will appear on ECR
![ECR](/images/ECR/5.png)
