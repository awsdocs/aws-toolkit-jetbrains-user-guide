# Update Code dialog box<a name="update-code-dialog"></a>

The **Update Code** dialog box in the AWS Toolkit for JetBrains is displayed whenever you [update an AWS Lambda function](key-tasks.md#key-tasks-sam-deploy)\.

![\[The Update Code dialog box.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **Update Code** dialog box contains the following items:

**Handler**  
\(Required\) The ID of the corresponding Lambda function handler for [Java](https://docs.aws.amazon.com/lambda/latest/dg/java-handler.html), [Python](https://docs.aws.amazon.com/lambda/latest/dg/python-handler.html), [Node\.js](https://docs.aws.amazon.com/lambda/latest/dg/nodejs-handler.html), or [C\#](https://docs.aws.amazon.com/lambda/latest/dg/csharp-handler.html)\.

**Source Bucket**  
\(Required for `Zip` package type only\) Choose an existing Amazon Simple Storage Service \(Amazon S3\) bucket in the connected AWS account for the AWS Serverless Application Model \(AWS SAM\) command line interface \(CLI\) to use to deploy the function to Lambda\. To create an Amazon S3 bucket in the account and have the AWS SAM CLI use that bucket instead, choose **Create**, and then follow the on\-screen instructions\. For information about Lambda package types, see [Lambda deployment packages](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html) in the *AWS Lambda Developer Guide*\.

**ECR Repository**  
\(Required for `Image` package type only\) Choose an existing Amazon Elastic Container Registry \(Amazon ECR\) repository in the connected AWS account for the AWS SAM CLI to use to deploy the function to Lambda\.