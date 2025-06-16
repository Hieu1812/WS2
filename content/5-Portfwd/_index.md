+++
title = "CodePipeline setup"
date = 2020
weight = 5
chapter = false
pre = "<b>5. </b>"
+++


We will configure **Code Pipeline** to automate the container deployment process with git push as the trigger.

#### Create CodePipeline

1. Access **Code Pipeline**
  ![cluster](/images/Codepl/1.png)
2. Select Pipeline -> Create Pipeline
  ![cluster](/images/Codepl/2.png)
  - Choose build custom pipeline -> next
  ![cluster](/images/Codepl/3.png)
  - Enter pipeline name, we'll create a new role and select next
  ![cluster](/images/Codepl/4.png)
  - For the Source, select github -> choose connection -> repository name -> branch. Select Webhook to trigger pipeline through push command
  {{% notice info %}}If you haven't set up the connection yet, you can refer to [here](URL "https://docs.aws.amazon.com/dtconsole/latest/userguide/connections-create-github.html#connections-create-github-console"){{% /notice %}}
  ![cluster](/images/Codepl/5.png)
  - For the build section, select Other build providers -> AWS Codebuild -> select the project created on page 3 and next
  ![cluster](/images/Codepl/6.png)
  - We'll skip the test section
  ![cluster](/images/Codepl/7.png)
  - For deployment, select ECS -> Choose cluster -> Service -> Next
  ![cluster](/images/Codepl/8.png)
  - Review and select Create pipeline
  ![cluster](/images/Codepl/9.png)
1. After creation, the pipeline will run and return a successful result.
  ![cluster](/images/Codepl/10.png)

#### Launch pipeline
- Execute git push command or select release change to start the pipeline.

Congratulations, you have completed the hands-on practice for creating a CI/CD pipeline. Remember to perform the resource cleanup step to avoid unwanted costs.

