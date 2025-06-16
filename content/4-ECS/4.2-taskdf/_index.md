+++
title = "Task Definition Setup"
date = 2020
weight = 1
chapter = false
pre = "<b>4.2 </b>"
+++

In this step, we will create a task definition for the cluster we just created.

#### Create **Task definition**

1. Access Task definition -> Create new task definition
![taskdf](/images/ECS/taskdf/1.png)

2. On the **Create bucket** page 
    - Enter Task definition name.
    - Select Launch type, here we choose fargate.
    - Operating system, CPU, RAM should be chosen based on application requirements.
    - For Task roles, select existing roles or create new ones in that section.
    ![taskdf](/images/ECS/taskdf/2.png)
3. In the container section, configure as follows
    - Enter container name.
    - For Image URI, enter the exact URI with image tag. You can also access ECR -> Required Repository -> Copy URI with the tag we need.
    - Open port for container, in our code we use port 3005 so we'll set port 3005
    - For resource limits, we'll use defaults. You can adjust CPU and RAM max/min limits according to your needs
    - For container environment variables, we recommend using Secrets manager. 
    - Select create to complete the setup
    ![taskdf](/images/ECS/taskdf/3.png)
4. After setup, it will display task definition details with active status indicating completion and we can move to the next step.
    ![taskdf](/images/ECS/taskdf/4.png)

