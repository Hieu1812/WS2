+++
title = "CodeBuild Setup"
date = 2020
weight = 3
chapter = false
pre = "<b>3. </b>"
+++"

In this section, you will set up CodeBuild to run dockerfile and store them on ECR

{{% notice info %}}
You will need to add buildspec.yaml for CodeBuild to work as intended. [Reference buildspec file](https://github.com/Hieu1812/book-server/blob/main/buildspec.yml)
{{% /notice %}}

### Create CodeBuild

1. Access **CodeBuild**
   ![Codebuild](/images/Codebuild/1.png)
2. Select Create project
   ![Codebuild](/images/Codebuild/2.png)
3. Enter the project name, select default as the project type.
4. In the Source section: CodeBuild will be triggered through GitHub repo push command, so we will select the source directly from our GitHub.
   ![Codebuild](/images/Codebuild/3.png)
   ![Codebuild](/images/Codebuild/4.png)
5. For environment settings, we will leave them as default. Then create a new service role and choose to use buildspec.yml file.
   ![Codebuild](/images/Codebuild/5.png)
6. For the Artifact section, select no artifacts and fill in the group name for easier log management. Then Create build project
   ![Codebuild](/images/Codebuild/6.png)
   At this point, CodeBuild setup is complete but we need to grant permissions to the newly created service role so CodeBuild has permission to push images to ECR
7. Access the service role from the CodeBuild details page
8. On the role details page, select Add permissions -> Attach policies
   ![Codebuild](/images/Codebuild/8.png)
9. Search for EC2Container, here we will choose the appropriate permission for this role as PowerUser. Then select Add permissions.
   ![Codebuild](/images/Codebuild/9.png)
10. CodeBuild is now ready to operate, you can trigger it through git push or select start build
    ![Codebuild](/images/Codebuild/10.png)
    ![Codebuild](/images/Codebuild/11.png)


