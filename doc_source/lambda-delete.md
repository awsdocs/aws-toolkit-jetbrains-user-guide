# Deleting an Lambda Function By Using the AWS Toolkit for JetBrains<a name="lambda-delete"></a>

You can use the AWS Toolkit to delete an AWS Lambda function that is part of an AWS serverless application, or you can delete a Lambda function by itself\.

To delete a Lambda function that is part of an AWS serverless application, skip the rest of this topic and see [Deleting an Application](sam-delete.md) instead\.

Otherwise, to delete a Lambda function by itself, do the following\.

1. [Open the AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](key-tasks.md#key-tasks-switch-region) that contains the function if necessary\.

1. Expand **Lambda**\.

1. Right\-click the name of the function to delete, and then choose **Delete Function**\.  
![\[Choosing the Delete Function command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Type the function's name to confirm the deletion, and then choose **OK**\. If the function deletion is successful, the AWS Toolkit removes the name of the function from the **Lambda** list\.