# Using Amazon SQS with AWS Lambda in the AWS Toolkit for JetBrains<a name="sqs-lambda"></a>

The following procedure details how to configure Amazon SQS queues as Lambda triggers in the AWS Toolkit for JetBrains\. 

**To configure an Amazon SQS queue as a Lambda triggers**

1. Open JetBrains\.

1. [Open AWS Explorer within the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-open-explorer)\.

1. Choose the Amazon SQS drop\-down arrow to expand your list of queues\.

1. Open the context \(right\-click\) menu for the queue you want to use and choose **Configure Lambda Trigger**\.

1. In the dialog box, from the drop\-down menu, choose the Lambda function that you want to trigger\.

1. Choose **Configure**\.

1. If the Lambda function lacks the necessary IAM permissions for Amazon SQS to run it, the toolkit generates a minimal policy that you can add to the IAM role for the Lambda function\. 

   Choose **Add Policy**\.

After you configure your queue, you get a status message about the applied changes, including any applicable error messages\.