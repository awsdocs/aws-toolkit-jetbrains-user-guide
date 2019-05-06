# Creating an AWS Serverless Application By Using the AWS Toolkit for JetBrains<a name="deploy-serverless-app"></a>

To complete this procedure, you must first [install the AWS Toolkit](key-tasks.md#key-tasks-install) and then [connect to an AWS account for the first time](key-tasks.md#key-tasks-first-connect), if you have not done so already\. Then, with IntelliJ IDEA or PyCharm already running, do the following\.

1. On the **File** menu, choose **New Project**\.

1. For IntelliJ IDEA, choose **AWS, AWS Serverless Application**, and then choose **Next**\.  
![\[Choosing to create an AWS serverless application in IntelliJ IDEA\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

   For PyCharm, choose **AWS Serverless Application**\.  
![\[Choosing to create an AWS serverless application in PyCharm\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Complete the [New Project dialog box](new-project-dialog.md), and then choose **Finish** \(for IntelliJ IDEA\) or **Create** \(for PyCharm\)\. The AWS Toolkit creates the project and adds the serverless application's code files to the new project\.

1. If you're using IntelliJ IDEA, with the **Project** tool window already open and displaying the project that contains the serverless application's files, do one of the following\.
   + For Maven based projects, right\-click the project's `pom.xml` file, and then choose **Add as Maven Project**\.  
![\[Choosing to add the POM file as a Maven project\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + For Gradle\-based projects, right\-click the project's `build.gradle` file, and then choose **Import Gradle project**\.  
![\[Choosing to import the Gradle project\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

     Complete the **Import Module from Gradle** dialog box, and then choose **OK**\.

After you create the serverless application, you can [run \(invoke\) or debug the local version of an AWS Lambda function](key-tasks.md#key-tasks-lambda-local) that is contained in that application\.

You can also [deploy the serverless application](key-tasks.md#key-tasks-sam-deploy)\. After you deploy it, you can [run \(invoke\) the remote version of a Lambda function](key-tasks.md#key-tasks-lambda-remote) that is part of that deployed application\.