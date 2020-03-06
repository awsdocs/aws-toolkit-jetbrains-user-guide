# Installing the AWS Toolkit for JetBrains<a name="setup-toolkit"></a>

Install the AWS Toolkit for JetBrains as follows\.

1. [Create an AWS account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/), if you don't have an account already\.

1.  [Create an administrator user and group in AWS Identity and Access Management \(IAM\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html#getting-started_create-admin-group-console) in the account, if you haven't done that already\. 
**Note**  
We recommend that you create or use a special type of user and group in the account for the AWS Toolkit for JetBrains to use, which we call an *administrator* IAM user and group\. Although you can [create a regular IAM user and group](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html#id_users_create_console) in the account for the toolkit to use, this approach might not allow the toolkit to have full access to all of the AWS resources and AWS serverless applications in that account\. \(We support, but [strongly discourage](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users), using an [AWS account root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials) with the AWS Toolkit for JetBrains\.\)

1. [Create an access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey) for the user, if you don't have an [access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) for that user already\. 
**Note**  
An access key contains both an *access key ID* value and a *secret access key* value\. The AWS Toolkit for JetBrains needs to use both of these values later\. Be sure to store them in a secure location\. If you lose them, they're gone forever and can't be retrieved\. However, you can always [delete a lost access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey), and then [create a replacement access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey)\. If you ever do this, you also need to [change your toolkit connection settings](key-tasks.md#key-tasks-change-connect)\. We support, but [strongly discourage](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users), [creating an access key for an AWS account root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html#id_root-user_manage_add-key) for the AWS Toolkit for JetBrains to use\.

1. Ensure that [IntelliJ IDEA, PyCharm, WebStorm, or JetBrains Rider](https://www.jetbrains.com/products.html) 2019\.2 or later is installed and running\.

1. Open **Settings** / **Preferences**\.

1. Choose **Plugins**\.

1. On the **Marketplace** tab, in **Search plugins in marketplace**, begin entering `AWS Toolkit`\. When **AWS Toolkit by Amazon Web Services** is displayed, choose it\.  
![\[Finding the AWS Toolkit\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Choose **Install**\.  
![\[Installing the AWS Toolkit for JetBrains\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
**Note**  
To use the AWS Toolkit for JetBrains to work with its available features for AWS CloudFormation, AWS Lambda, AWS Serverless, and Amazon ECS, you must install version 1\.8 or later of the AWS Toolkit\.

1. When the **Third\-party Plugins Privacy Note** is displayed, choose **Accept**\.

1. Choose **Restart IDE**\.

1. When prompted, choose **Restart**\.

1. Before you can use the AWS Toolkit for JetBrains to develop, test, analyze, and deploy AWS serverless applications or AWS Lambda functions, you must first also install the following tools, if you haven't done so already\. These tools must be installed in the following order:

   1. [AWS Command Line Interface \(AWS CLI\)](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html)

   1. [Docker](https://docs.docker.com/install/) \(Docker must always be running whenever you develop, test, analyze, or deploy serverless applications or functions\)

   1. [AWS Serverless Application Model Command Line Interface \(AWS SAM CLI\)](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)

1. Before you can use the AWS Toolkit for JetBrains to debug code in Amazon ECS clusters, you must also complete additional steps\. For instructions, see the [prerequisites](ecs-debug.md#ecs-prereqs)\.

1. After you install the AWS Toolkit for JetBrains \(and, if you're working with AWS serverless applications, Lambda functions, or Amazon ECS clusters, you've installed the preceding additional required tools, in order\), [connect to an AWS account for the first time](key-tasks.md#key-tasks-first-connect)\.

## Installing AWS Toolkit for JetBrains Early Access Program \(EAP\) Builds<a name="eap-or-custom-install"></a>

AWS occasionally releases AWS Toolkit for JetBrains preview and experimental plugins and features through Early Access Program \(EAP\) builds\.

You can automatically get updated EAP builds as they become available, as follows\.

1. Make sure IntelliJ IDEA, PyCharm, WebStorm, or JetBrains Rider is running\.

1. Open **Settings** / **Preferences**\.

1. Choose **Plugins**\.

1. Choose **Manage Repositories, Configure Proxy or Install Plugin from Disk** \(the gear icon\)\.

1. Choose **Manage Plugin Repositories**\.

1. Choose **Add** \(the **\+** icon\)\.

1. Enter the following URL to the EAP repository for the AWS Toolkit for JetBrains: `https://plugins.jetbrains.com/plugins/eap/aws.toolkit`\. Then press Enter, and choose **OK**\.

1. If prompted, choose **Restart IDE**\. Then when prompted, choose **Restart**\.

1. Now, whenever a later EAP build is available, choose **Update** next to the** AWS Toolkit** entry in **Plugins**\. When prompted, choose **Restart IDE**\. Then choose **Restart**\.

1. To remove a reference to the custom repository, in the **Preferences** dialog, choose **Plugins**\. Then choose **Manage Repositories, Configure Proxy or Install Plugin from Disk** \(the gear icon\), **Manage Plugin Repositories**\. Select the URL to the custom repository, and then choose **Remove** \(the **\-** icon\)\. Then choose **OK**\.