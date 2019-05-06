# Creating an AWS Lambda Function By Using the AWS Toolkit for JetBrains<a name="create-new-lambda"></a>

You can use the AWS Toolkit to create an AWS Lambda function that is part of an AWS serverless application, or you can create a Lambda function by itself\.

To create a Lambda function that is part of an AWS serverless application, skip the rest of this topic and see [Creating an Application](deploy-serverless-app.md) instead\.

To create a Lambda function by itself, you must first [install the AWS Toolkit](key-tasks.md#key-tasks-install) and then [connect to an AWS account for the first time](key-tasks.md#key-tasks-first-connect), if you have not done so already\. Then, with IntelliJ IDEA or PyCharm already running, do one of the following\.
+ [Open the AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](key-tasks.md#key-tasks-switch-region) to create the function in if necessary\. Right\-click **Lambda**, and then choose **Create new AWS Lambda**\.  
![\[Choosing to create an AWS Lambda function starting from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

  Complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\. The AWS Toolkit creates a corresponding AWS CloudFormation stack for the deployment and adds the name of the function to the **Lambda** list in the **AWS Explorer**\. If the deployment fails, you can try to figure out why by [viewing event logs for the stack](key-tasks.md#key-tasks-cloudformation-logs)\.
+ Create a code file that implements a [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or a [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html)\. 

  To enable running \(invoking\) the remote version of the function, you must also [switch to a different AWS Region](key-tasks.md#key-tasks-switch-region) to create the function in if necessary\. Then, in the code file, choose the **Lambda** icon in the gutter next to the function handler, and then choose **Create new AWS Lambda**\. Complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\.  
![\[Choosing to create an AWS Lambda function starting from an existing function handler in a code file\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
**Note**  
If the **Lambda** icon does not display in the gutter next to the function handler, you can try displaying it for the current project by selecting the following box in **Preferences**: **Tools, AWS, Project settings, Show gutter icons for all potential AWS Lambda handlers**\. Also, the **Create new AWS Lambda** command won't display if the function handler is already defined in the corresponding AWS SAM template\.

  After you choose **Create Function**, the AWS Toolkit creates a corresponding function in the Lambda service for the connected AWS account\. If the operation succeeds, after you refresh the **AWS Explorer**, the **Lambda** list displays the name of the new function\.
+ If you already have a project that contains an AWS Lambda function, first [switch to a different AWS Region](key-tasks.md#key-tasks-switch-region) to create the function in if necessary\. Then, in the code file that contains the [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or the [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html), choose the **Lambda** icon in the gutter next to the function handler\. Choose **Create new AWS Lambda**, complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\.  
![\[Choosing to create an AWS Lambda function starting from an existing function handler in a code file\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
**Note**  
If the **Lambda** icon does not display in the gutter next to the function handler, you can try displaying it for the current project by selecting the following box in **Preferences**: **Tools, AWS, Project settings, Show gutter icons for all potential AWS Lambda handlers**\. Also, the **Create new AWS Lambda** command won't display if the function handler is already defined in the corresponding AWS SAM template\.

  After you choose **Create Function**, the AWS Toolkit creates a corresponding function in the Lambda service for the connected AWS account\. If the operation succeeds, after you refresh the **AWS Explorer**, the **Lambda** list displays the name of the new function\.

After you create the function, you can [run \(invoke\) or debug the local version of the function](key-tasks.md#key-tasks-lambda-local) or [run \(invoke\) the remote version](key-tasks.md#key-tasks-lambda-remote)\.