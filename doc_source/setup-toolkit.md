# Installing the AWS Toolkit for JetBrains<a name="setup-toolkit"></a>

Install the AWS Toolkit for JetBrains as follows\.

1. [Create an AWS account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/), if you don't have an account already\.

1.  [Create an administrator user and group in AWS Identity and Access Management \(IAM\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html#getting-started_create-admin-group-console) in the account, if you haven't already done so\. 
**Note**  
We recommend that you create or use a special type of user and group in the account for the AWS Toolkit to use, which we call an *administrator* IAM user and group\. While you can [create a regular IAM user and group](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html#id_users_create_console) in the account for the AWS Toolkit to use, this approach might not allow the AWS Toolkit to have full access to all of the AWS resources and AWS serverless applications in that account\. \(We support, but [strongly discourage](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users), using an [AWS account root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials) with the AWS Toolkit\.\)

1. [Create an access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey) for the user, if you don't have an [access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) for that user already\. 
**Note**  
An access key contains both an *access key ID* value and a *secret access key* value\. The Toolkit will need to use both of these values later\. Be sure to store them in a secure location\. If you lose them, they're gone forever and cannot be retrieved\. However, you can always [delete a lost access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey) and then [create a replacement access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey) if needed\. If you ever do this, you'll also need to [change your AWS Toolkit connection settings](key-tasks.md#key-tasks-change-connect)\. \(We support, but [strongly discourage](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users), [creating an access key for an AWS account root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html#id_root-user_manage_add-key) for the AWS Toolkit to use\.\)

1. Have [IntelliJ IDEA or PyCharm](https://www.jetbrains.com/products.html) 2018\.3 or later installed and running\.

1. For macOS, on the main menu, choose **IntelliJ IDEA, Preferences** or **PyCharm, Preferences**\. For other operating systems, on the main menu, choose **File, Settings**\. 

1. Choose **Plugins**\.

1. On the **Marketplace** tab, in **Search plugins in marketplace**, begin typing `AWS Toolkit`\. When **AWS Toolkit by Amazon Web Services** displays, choose it\.  
![\[Finding the AWS Toolkit\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Choose **Install**\.  
![\[Installing the AWS Toolkit\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. When the **Third\-party Plugins Privacy Note** displays, choose **Accept**\.

1. Choose **Restart IDE**\.

1. When prompted, choose **Restart**\.

1. Before you can use the AWS Toolkit to develop, test, analyze, and deploy AWS serverless applcations or AWS Lambda functions, you must first also install the following tools, in this order, if you haven't done so already\.

   1. The [AWS Command Line Interface \(AWS CLI\)](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html)

   1. [Docker](https://docs.docker.com/install/) \(Docker must always be running whenever you develop, test, analyze, or deploy serverless applcations or functions\)

   1. The [AWS Serverless Application Model Command Line Interface \(AWS SAM CLI\)](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)

1. After you install the AWS Toolkit \(and, if you're working with AWS serverless applications or Lambda functions, the preceding additional required tools\), [connect to an AWS account for the first time](key-tasks.md#key-tasks-first-connect)\.