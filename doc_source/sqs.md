# Working with Amazon SQS by using the AWS Toolkit for JetBrains<a name="sqs"></a>

The following topics describe how to use the AWS Toolkit for JetBrains to work with Amazon SQS\.

Standard and FIFO \(First\-In\-Last\-Out\) are the two kinds of messages you can send using Amazon SQS in the AWS Toolkit for JetBrains\. 

**To create an Amazon SQS queue**

1. Open JetBrains\.

1. [Open AWS Explorer within the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-open-explorer)\.

1. Open the context \(right\-click\) menu for **SQS**, and choose **Create Queue\.\.\.**\.

1. Provide a queue name and choose the queue type \(either **Standard** or **FIFO**\. For more information on queue types, see the following topics in the *Amazon Simple Queue Service Developer Guide*:
   + [Amazon SQS standard queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/standard-queues.html)
   + [Amazon SQS FIFO \(First\-In\-First\-Out\) queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html)

1. Choose **Create**\.

**To view Amazon SQS messages**

1. Open JetBrains\.

1. [Open AWS Explorer within the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-open-explorer)\.

1. Choose the Amazon SQS drop\-down arrow to expand your list of queues\.

1. Open the context \(right\-click\) menu for that queue and choose **View Messages**\.

1. Choose **View Messages** to view the messages in this queue\. Up to ten messages will be polled\. Messages are immediately returned to the queue after being shown\. For information about polling, see [Amazon SQS short and long polling](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html) in the *Amazon Simple Queue Service Developer Guide*\.

**To edit Amazon SQS queue properties**

1. Open JetBrains\.

1. [Open AWS Explorer within the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-open-explorer)\.

1. Choose the Amazon SQS drop\-down arrow to expand your list of queues\.

1. Open the context \(right\-click\) menu for the queue that you want to edit and choose **Edit Queue Properties\.\.\.**\.

1. In the **Edit Queue Properties** dialog box that opens, review and modify your queue properties\. For more information on Amazon SQS properties, see [Configuring queue parameters \(console\)](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-configure-queue-parameters.html) in the *Amazon Simple Queue Service Developer Guide*\.

**To send Standard messages**

1. Open JetBrains\.

1. [Open AWS Explorer within the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-open-explorer)\.

1. Choose the Amazon SQS drop\-down arrow to expand your list of queues\.

1. Open the context \(right\-click\) menu for that queue and choose **Send a message**\.

1. Populate the message and choose **Send**\. After you send the message, you see a confirmation that includes the message ID\.

**To send FIFO messages**

1. Open JetBrains\.

1. [Open AWS Explorer within the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-open-explorer)\.

1. Choose the Amazon SQS drop\-down arrow to expand your list of queues\.

1. Open the context \(right\-click\) menu for that queue and choose **Send a message**\.

1. Populate the message, group id, and an optional deduplication id\.
**Note**  
If no deduplication id is provided, one will be generated\.

1. Choose **Send**\. After you send the message, you see a confirmation that includes the message ID\.

**To delete an Amazon SQS queue**

1. To verify that a queue is empty before you delete it, see [COnfirming that a queue is empty](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/confirm-queue-is-empty.html) in the *Amazon Simple Queue Service Developer Guide*\.

1. Open JetBrains\.

1. [Open AWS Explorer within the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-open-explorer)\.

1. Open the context \(right\-click\) menu for on **SQS**, and choose **Delete Queue\.\.\.**\.

1. Confirm that you want to delete the queue, and choose **OK** in the deletion dialog box\.

**Topics**
+ [Using Amazon SQS with AWS Lambda in the AWS Toolkit for JetBrains](sqs-lambda.md)
+ [Using Amazon SQS with Amazon SNS in the AWS Toolkit for JetBrains](sqs-sns.md)