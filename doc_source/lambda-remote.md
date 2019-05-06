# Running \(Invoking\) the Remote Version of an AWS Lambda Function By Using the AWS Toolkit for JetBrains\.<a name="lambda-remote"></a>

A *remote* version of an AWS Lambda function is a function whose source code already exists inside of the Lambda service for an AWS account\.

To complete this procedure, you must first [install the AWS Toolkit](key-tasks.md#key-tasks-install) and then [connect to an AWS account for the first time](key-tasks.md#key-tasks-first-connect), if you have not done so already\. Then, with IntelliJ IDEA or PyCharm already running, do the following\.

1. [Open the AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](key-tasks.md#key-tasks-switch-region) that contains the function if necessary\.

1. Expand **Lambda**, and confirm that the name of the function is listed\. If it is listed, skip ahead to step 3 in this procedure\.

   If the name of the function is not listed, [create the Lambda function](key-tasks.md#key-tasks-lambda-create) that you want to run \(invoke\), if you have not done so already\. 

   If you created the function as [part of an AWS serverless application](key-tasks.md#key-tasks-lambda-create-app), you must also [deploy that application](key-tasks.md#key-tasks-sam-deploy)\.

   If you created the function by creating a code file that implements a [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or a [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html), then in the code file, choose the Lambda icon next to the function handler, and then choose **Create new AWS Lambda**\. Complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\.

1. With **Lambda** already expanded in the **AWS Explorer**, right\-click the name of the function, and then choose **Run '\[Remote\]'**\.  
![\[Choosing to run the remote version of a Lambda function starting from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Complete the [Edit configuraton dialog](edit-configuration-dialog.md) box if it displays, and then choose **Run**\. \(If the **Edit configuration** dialog box doesn't display and you want to change the existing configuration, [change its configuration](key-tasks.md#key-tasks-lambda-update), and then repeat from step 3 in this procedure\. If the configuration details are missing, first expand **Templates, AWS Lambda**, and then choose **Remote**; choose **OK**; and then repeat this procedure from the beginning\.\) Results are displayed in the **Run** tool window\. 