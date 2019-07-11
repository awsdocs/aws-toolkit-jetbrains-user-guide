# Deleting an AWS Serverless Application By Using the AWS Toolkit for JetBrains<a name="sam-delete"></a>

You must first [deploy the AWS serverless application](key-tasks.md#key-tasks-sam-deploy) that you want to delete, if you haven't deployed it already\.

1. [Open the AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](key-tasks.md#key-tasks-switch-region) that contains the serverless application if necessary\.

1. Expand **CloudFormation**\.

1. Right\-click the name of the AWS CloudFormation stack that contains the serverless application you want to delete, and then choose **Delete CloudFormation Stack**\.  
![Choosing to delete the AWS CloudFormation stack for an AWS serverless application starting from the AWS Explorer](https://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/images/sam-delete.png)

1. Type the stack's name to confirm the deletion, and then choose **OK**\. If the stack deletion is successful, the AWS Toolkit removes the name of the stack from the **CloudFormation** list in the **AWS Explorer**\. If the stack deletion fails, you can try to figure out why by [viewing event logs for the stack](key-tasks.md#key-tasks-cloudformation-logs)\.
