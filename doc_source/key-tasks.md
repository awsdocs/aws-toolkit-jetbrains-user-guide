# Key Tasks for the AWS Toolkit for JetBrains<a name="key-tasks"></a>

Use the following brief instructions to complete key tasks with the AWS Toolkit for JetBrains\.
+ [Install the AWS Toolkit](#key-tasks-install)
+ [Update the AWS Toolkit](#key-tasks-update)
+ [Configure the AWS Toolkit to use an HTTP proxy](#key-tasks-proxy)
+ [Work with connections from the AWS Toolkit to AWS accounts](#key-tasks-connections)
  + [Connect to an AWS account for the first time](#key-tasks-first-connect)
  + [Get the current connection](#key-tasks-current-connect)
  + [Add multiple connections](#key-tasks-multiple-connect)
  + [Switch between connections](#key-tasks-switch-connect)
  + [Change connection settings](#key-tasks-change-connect)
  + [Delete a connection](#key-tasks-delete-connect)
+ [Get the current AWS Region that the AWS Toolkit is using](#key-tasks-current-region)
+ [Switch between Regions](#key-tasks-switch-region)
+ [Open the AWS Explorer within the AWS Toolkit](#key-tasks-open-explorer)
+ [Work with AWS serverless applications in an account](#key-tasks-open-explorer)
  + [Create a serverless applications](#key-tasks-sam-create)
  + [Deploy a serverless application](#key-tasks-sam-deploy)
  + [Change \(update\) the settings for a serverless application](#key-tasks-sam-update)
  + [Delete a serverless application](#key-tasks-sam-delete)
+ [Work with AWS Lambda functions in an account](#key-tasks-lambda)
  + [Create a function](#key-tasks-lambda-create)
  + [Run \(invoke\) or debug the local version of a function](#key-tasks-lambda-local)
  + [Run \(invoke\) the remote version of a function](#key-tasks-lambda-remote)
  + [Change \(update\) the configuration for a function](#key-tasks-lambda-update)
  + [Delete a function](#key-tasks-lambda-delete)
+ [Work with AWS CloudFormation stacks in an account](#key-tasks-cloudformation)
  + [View event logs for a stack](#key-tasks-cloudformation-logs)
  + [Delete a stack](#key-tasks-cloudformation-delete)

## Installing the AWS Toolkit for JetBrains<a name="key-tasks-install"></a>

1. [Create an AWS account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/), if you don't have an account already\.

1.  [Create an administrator user and group in AWS Identity and Access Management \(IAM\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html#getting-started_create-admin-group-console) in the account, if you haven't already done so\. 
**Note**  
We recommend that you create or use a special type of user and group in the account for the AWS Toolkit to use, which we call an *administrator* IAM user and group\. While you can [create a regular IAM user and group](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html#id_users_create_console) in the account for the AWS Toolkit to use, this approach might not allow the AWS Toolkit to have full access to all of the AWS resources and AWS serverless applications in that account\. \(We support, but [strongly discourage](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users), using an [AWS account root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials) with the AWS Toolkit\.\)

1. [Create an access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey) for the user, if you don't have an [access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) for that user already\. 
**Note**  
An access key contains both an *access key ID* value and a *secret access key* value\. The Toolkit will need to use both of these values later\. Be sure to store them in a secure location\. If you lose them, they're gone forever and cannot be retrieved\. However, you can always [delete a lost access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey) and then [create a replacement access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey) if needed\. If you ever do this, you'll also need to [change your AWS Toolkit connection settings](#key-tasks-change-connect)\. \(We support, but [strongly discourage](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users), [creating an access key for an AWS account root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html#id_root-user_manage_add-key) for the AWS Toolkit to use\.\)

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

1. After you install the AWS Toolkit \(and, if you're working with AWS serverless applications or Lambda functions, the preceding additional required tools\), [connect to an AWS account for the first time](#key-tasks-first-connect)\.

[Top](#key-tasks)

## Updating the AWS Toolkit<a name="key-tasks-update"></a>

After you have [installed the AWS Toolkit for JetBrains](#key-tasks-install), you can check for updates to the AWS Toolkit at any time and install any that exist\. To do this, with IntelliJ IDEA or PyCharm already running, do the following\.

1. For macOS, on the main menu, choose **IntelliJ IDEA, Preferences** or **PyCharm, Preferences**\. For other operating systems, on the main menu, choose **File, Settings**\.

1. Choose **Updates**\. \(If no updates display, you might need to choose **Check new updates**\.\)  
![\[Checking for updates to the AWS Toolkit\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Follow any on\-screen instructions to finish updating the AWS Toolkit\.

1. After you finish updating the AWS Toolkit, restart IntelliJ IDEA or PyCharm\. 

## Configuring the AWS Toolkit to Use an HTTP Proxy<a name="key-tasks-proxy"></a>

After you have [installed the AWS Toolkit for JetBrains](#key-tasks-install), you can configure it to use an HTTP proxy\. To do this, with IntelliJ IDEA or PyCharm already running, do one of the following\.
+ For IntelliJ IDEA, see [HTTP Proxy](https://www.jetbrains.com/help/idea/settings-http-proxy.html) on the IntelliJ IDEA Help website\.
+ For PyCharm, see [HTTP Proxy](https://www.jetbrains.com/help/pycharm/settings-http-proxy.html) on the PyCharm Help website\.

After you complete the preceding instructions, the AWS Toolkit begins using those HTTP proxy settings\.

## Connecting the AWS Toolkit to AWS Accounts<a name="key-tasks-connections"></a>

After you have [installed the AWS Toolkit for JetBrains](#key-tasks-install), use the AWS Toolkit to do the following with AWS accounts\.
+ [Connect to an AWS account for the first time](#key-tasks-first-connect)
+ [Get the current connection](#key-tasks-current-connect)
+ [Add multiple connections](#key-tasks-multiple-connect)
+ [Switch between connections](#key-tasks-switch-connect)
+ [Change connection settings](#key-tasks-change-connect)
+ [Delete a connection](#key-tasks-delete-connect)

[Top](#key-tasks)

### Connecting for the First Time<a name="key-tasks-first-connect"></a>

Assuming that you have already [installed the AWS Toolkit](#key-tasks-install), then to complete this procedure, you must first have an [access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) \(which contains both an *access key ID* value and a *secret access key* value\) for a user in IAM \(which we recommend\) or AWS account root user \(which we strongly discourage\)\. \(If you don't have an access key for a user in IAM already, [create one](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey)\.\)

1. With your access key ID value and secret access key value ready, do one of the following\.
   + On the status bar, choose **AWS: No credentials selected**, and then choose **Edit AWS Credential file\(s\)**\.  
![\[AWS no credentials selected on the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)  
![\[Edit AWS credentials from the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open\. Choose **Configure AWS Connection**, and then choose **Edit AWS Credential file\(s\)**\.  
![\[Configure AWS connection from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)  
![\[Edit AWS credentials from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. In the file, next to `[default]`, for `aws_access_key_id`, replace `[accessKey1]` with your access key ID value \(for example, `AKIAIOSFODNN7EXAMPLE`\)\.

   If prompted, select **I want to edit this file anyway**, and then choose **OK**\.

1. For `aws_secret_access_key`, replace `[secretKey1]` with your secret access key value \(for example, `wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY`\)\.

   The final results should look as follows, following the [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) format\.

   ```
   ... Other file contents omitted for brevity ...
   
   [default]
   # ... Some comments ...
   aws_access_key_id = AKIAIOSFODNN7EXAMPLE
   # ... Some more comments ...
   # ... Some more comments ...
   # ... Some more comments ...
   # ... Some more comments ...
   aws_secret_access_key = wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
   
   ... Other file contents omitted for brevity ...
   ```
**Note**  
The AWS Toolkit currently supports the following configuration variables\.  
`aws_access_key_id`
`aws_secret_access_key`
`aws_session_token`
`credential_process`
`mfa_serial`
`role_arn`
`source_profile`
For more information, see [AWS CLI Configuration Variables](https://docs.aws.amazon.com/cli/latest/topic/config-vars.html) in the *AWS CLI Command Reference*\.

1. Save and then close the file\. The AWS Toolkit attempts to connect to the account by using the preceding access key\. After connecting, you can use the AWS Toolkit to work with AWS resources in that account such as [AWS serverless](#key-tasks-sam) applications, [AWS Lambda](#key-tasks-lambda) functions, and [AWS CloudFormation](#key-tasks-cloudformation) stacks\.

You can also have [more than one connection](#key-tasks-multiple-connect) available, so that you can [switch between them](#key-tasks-switch-connect), if you want\.

After you connect, the AWS Toolkit selects the default AWS Region automatically\. You might need to [switch to working with AWS resources in that account that are in a different Region](#key-tasks-switch-region)\.

[Top](#key-tasks)

### Adding Multiple Connections<a name="key-tasks-multiple-connect"></a>

To complete this procedure, you must first have the additional [access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) \(which contains both an *access key ID* value and a *secret access key* value\) for a user in IAM \(which we recommend\) or AWS account root user \(which we strongly discourage\)\. \(If you don't have an access key for a user IAM already, [create one](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey)\.\)

1. [Connect for the first time](#key-tasks-first-connect), if you have not done so already\.

1. With the additional access key ID value and secret access key value ready, do one of the following\.
   + On the status bar, choose **AWS Connection Settings**, and then choose **All Credentials, Edit AWS Credential file\(s\)**\.  
![\[Choosing to edit AWS credentials from the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, and then choose **Show Options Menu** \(the gear icon\)\. Choose **AWS Connection Settings, All Credentials, Edit AWS Credential file\(s\)**\.  
![\[Choosing to edit AWS credentials from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. In the file, add a [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) for each additional connection\. Profile names can contain only the letters `A` through `Z`, the letters `a` through `z`, the numbers `0` through `9`, the hyphen character \(`-`\), and the underscore character \(`_`\)\. Profile names must be less than 64 characters in length\. 

   For example, for a named profile named `myuser`, use the following format\.

   ```
   [profile myuser]
   aws_access_key_id = AKIAIOSFODNN7EXAMPLE
   aws_secret_access_key = wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
   ```
**Note**  
The AWS Toolkit currently supports named profiles with only the following characters: `A`\-`Z`, `a`\-`z`, `0`\-`9`, underscore \(`_`\), and dash \(`-`\)\.  
The AWS Toolkit also currently supports only the following configuration variables\.  
`aws_access_key_id`
`aws_secret_access_key`
`aws_session_token`
`credential_process`
`mfa_serial`
`role_arn`
`source_profile`
For more information, see [AWS CLI Configuration Variables](https://docs.aws.amazon.com/cli/latest/topic/config-vars.html) in the *AWS CLI Command Reference*\.

1. Save and then close the file\. The AWS Toolkit displays the new connection in the **AWS Connection Settings** menu in both the status bar and in the **AWS Explorer**\.

Now that you have multiple connections, you can [switch between them](#key-tasks-switch-connect), if you want\.

After you connect, you might need to [switch to working with AWS resources in that account that are in a different AWS Region](#key-tasks-switch-region)\.

[Top](#key-tasks)

### Switching Between Connections<a name="key-tasks-switch-connect"></a>

1. [Add multiple connections](#key-tasks-multiple-connect), if you have not done so already\.

1. Do one of the following:
   + On the status bar, choose **AWS Connection Settings**\.
   + [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, and then choose **AWS Connection Settings**\.

1. Choose the name of the [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) that you want to use for the new connection\. If it is not listed, first choose **All Credentials**, and then choose the name of the named profile that you want to use\.   
![\[Switching the current connection\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

   The AWS Toolkit switches to using the new connection, which is now selected in the **AWS Connection Settings** menu in both the status bar and the **AWS Explorer**\.

After you connect, you might need to [switch to working with AWS resources in that account that are in a different AWS Region](#key-tasks-switch-region)\.

[Top](#key-tasks)

### Changing Connection Settings<a name="key-tasks-change-connect"></a>

1. Do one of the following:
   + On the status bar, choose **AWS Connection Settings, All Credentials, Edit AWS Credentials file\(s\)**\.  
![\[Choosing the Edit Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, and then choose **Show Options Menu** \(the gear icon\)\. Then choose **AWS Connection Settings, All Credentials, Edit AWS Credential file\(s\)**\.  
![\[Choosing the Edit Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Make your changes to the file, and then save and close the file\. 

[Top](#key-tasks)

### Deleting a Connection<a name="key-tasks-delete-connect"></a>

1. Do one of the following:
   + On the status bar, choose **AWS Connection Settings, All Credentials, Edit AWS Credentials file\(s\)**\.  
![\[Choosing the Edit Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, and then choose **Show Options Menu** \(the gear icon\)\. Then choose **AWS Connection Settings, All Credentials, Edit AWS Credential file\(s\)**\.  
![\[Choosing the Edit Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. In the file, completely delete the [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) \(including the named profile's name, access key ID, and secret access key\) for the connection that you want to delete\.

1. Save and then close the file\. The AWS Toolkit removes the deleted connection from the **AWS Connection Settings** menu in both the status bar and in the **AWS Explorer**\.

After you delete a connection, you might need to [switch to a different connection](#key-tasks-switch-connect) or [connect for the first time](#key-tasks-first-connect) again\.

[Top](#key-tasks)

## Getting the Current Connection<a name="key-tasks-current-connect"></a>

To check which connection the AWS Toolkit is currently using, do one of the following\.
+ On the status bar, the current connection is displayed in the **AWS Connection Settings** area\.  
![\[The current connection in the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
+ [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, and then choose **Show Options Menu** \(the gear icon\)\. Choose **AWS Connection Settings**\. The current connection is selected\.  
![\[The current connections in the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

You can also have [more than one connection](#key-tasks-multiple-connect) available, so that you can [switch between them](#key-tasks-switch-connect), if you want\.

[Top](#key-tasks)

## Getting the Current AWS Region<a name="key-tasks-current-region"></a>

To check which AWS Region the AWS Toolkit is currently using, do one of the following\.
+ On the status bar, the current Region is displayed in the **AWS Connection Settings** area\.  
![\[The current AWS Region in the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
+ [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, and then choose **Show Options Menu** \(the gear icon\)\. Choose **AWS Connection Settings**\. The current Region is selected\.  
![\[The current AWS Region in the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

You can also [switch to a different AWS Region](#key-tasks-switch-region), if you want\.

[Top](#key-tasks)

## Switching AWS Regions<a name="key-tasks-switch-region"></a>

Do one of the following\.
+ On the status bar, choose **AWS Connection Settings**, and then choose the AWS Region that you want to switch to\.  
![\[Choosing a different AWS Region in the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
+ [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open\. Choose **Show Options Menu** \(the gear icon\), and then choose **AWS Connection Settings**\. If the AWS Region that you want to switch to is listed, choose it\. Otherwise, choose **All Regions**, and then choose the Region that you want to switch to\.  
![\[Choosing a different AWS Region in the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The AWS Toolkit switches to using the new Region, which is now selected in the **AWS Connection Settings** menu in both the status bar and the **AWS Explorer**\.

[Top](#key-tasks)

## Opening the AWS Explorer<a name="key-tasks-open-explorer"></a>

To complete this procedure, you must first [install the AWS Toolkit](#key-tasks-install)\. Then, with IntelliJ IDEA or PyCharm already running, do one of the following\.
+ On the tool window bar, choose **AWS Explorer**\.  
![\[The AWS Explorer tool window button\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
+ On the **View** menu, choose **Tool Windows, AWS Explorer**\.  
![\[Opening the AWS Explorer from the main menu\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

After you open the **AWS Explorer** for the first time, use it to [connect to an AWS account for the first time](#key-tasks-first-connect)\. After you connect for the first time, you can then use the **AWS Explorer** to work with [AWS Lambda](#key-tasks-lambda) functions and [AWS CloudFormation](#key-tasks-cloudformation) stacks in the account\.

[Top](#key-tasks)

## Working with AWS Serverless Applications<a name="key-tasks-sam"></a>

After you have [installed the AWS Toolkit for JetBrains](#key-tasks-install) and then used the AWS Toolkit to [connect to an AWS account for the first time](#key-tasks-first-connect), you can use the AWS Toolkit to work with AWS serverless applications in an account as follows\.
+ [Create a serverless applications](#key-tasks-sam-create)
+ [Deploy a serverless application](#key-tasks-sam-deploy)
+ [Change \(update\) the settings for a serverless application](#key-tasks-sam-update)
+ [Delete a serverless application](#key-tasks-sam-delete)

[Top](#key-tasks)

### Creating a Serverless Application<a name="key-tasks-sam-create"></a>

To complete this procedure, you must first [install the AWS Toolkit](#key-tasks-install) and then [connect to an AWS account for the first time](#key-tasks-first-connect), if you have not done so already\. Then, with IntelliJ IDEA or PyCharm already running, do the following\.

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

After you create the serverless application, you can [run \(invoke\) or debug the local version of an AWS Lambda function](#key-tasks-lambda-local) that is contained in that application\.

You can also [deploy the serverless application](#key-tasks-sam-deploy)\. After you deploy it, you can [run \(invoke\) the remote version of a Lambda function](#key-tasks-lambda-remote) that is part of that deployed application\.

[Top](#key-tasks)

### Deploying a Serverless Application<a name="key-tasks-sam-deploy"></a>

To complete this procedure, you must first [create the AWS serverless application](#key-tasks-sam-create) that you want to deploy, if you haven't created it already\.
**Note**  
If you want to deploy a serverless application that contains an AWS Lambda function, and you want to deploy that function with any non\-default or optional properties, you must first set those properties in the function's corresponding AWS SAM template file \(for example, in a file named `template.yaml` within the project\)\. For a list of available properties, see [AWS::Serverless::Function](https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md#awsserverlessfunction) in the [awslabs/serverless\-application\-model](https://github.com/awslabs/serverless-application-model/) repository on the GitHub website\.

1. [Switch to a different AWS Region](#key-tasks-switch-region) to deploy the serverless application to if necessary\.

1. With the **Project** tool window already open and displaying the project that contains the serverless application's files, right\-click the project's `template.yaml` file, and then choose **Deploy Serverless Application**\.  
![\[Choosing the Deploy Serverless Application command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Complete the [Deploy Serverless Application dialog](deploy-serverless-application-dialog.md) box, and then choose **Deploy**\. The AWS Toolkit creates a corresponding AWS CloudFormation stack for the deployment and adds the name of the stack to the **CloudFormation** list in the **AWS Explorer**\. If the deployment fails, you can try to figure out why by [viewing event logs for the stack](#key-tasks-cloudformation-logs)\.

After you deploy it, you can [run \(invoke\) the remote version of an AWS Lambda function](#key-tasks-lambda-remote) that is part of that deployed application\.

[Top](#key-tasks)

### Changing \(Updating\) the Settings for a Serverless Application<a name="key-tasks-sam-update"></a>

You must first [deploy the AWS serverless application](#key-tasks-sam-deploy) that you want to change, if you haven't deployed it already\.
**Note**  
If you want to deploy a serverless application that contains an AWS Lambda function, and you want to deploy that function with any non\-default or optional properties, you must first set those properties in the function's corresponding AWS SAM template file \(for example, in a file named `template.yaml` within the project\)\. For a list of available properties, see [AWS::Serverless::Function](https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md#awsserverlessfunction) in the [awslabs/serverless\-application\-model](https://github.com/awslabs/serverless-application-model/) repository on the GitHub website\.

1. With the **Project** tool window already open and displaying the project that contains the serverless application's files, open the project's `template.yaml` file, change the file's contents to reflect the new settings, and then save and close the file\.

1. [Switch to a different AWS Region](#key-tasks-switch-region) to deploy the serverless application to if necessary\.

1. Right\-click the project's `template.yaml` file, and then choose **Deploy Serverless Application**\.  
![\[Choosing the Deploy Serverless Application command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Complete the [Deploy Serverless Application dialog](deploy-serverless-application-dialog.md) box, and then choose **Deploy**\. The AWS Toolkit updates the corresponding AWS CloudFormation stack for the deployment\. If the deployment fails, you can try to figure out why by [viewing event logs for the stack](#key-tasks-cloudformation-logs)\.

[Top](#key-tasks)

### Deleting a Serverless Application<a name="key-tasks-sam-delete"></a>

You must first [deploy the AWS serverless application](#key-tasks-sam-deploy) that you want to delete, if you haven't deployed it already\.

1. [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](#key-tasks-switch-region) that contains the serverless application if necessary\.

1. Expand **CloudFormation**\.

1. Right\-click the name of the AWS CloudFormation stack that contains the serverless application you want to delete, and then choose **Delete CloudFormation Stack**\.  
![\[Choosing to delete the AWS CloudFormation stack for an AWS serverless application starting from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Type the stack's name to confirm the deletion, and then choose **OK**\. If the stack deletion is successful, the AWS Toolkit removes the name of the stack from the **CloudFormation** list in the **AWS Explorer**\. If the stack deletion fails, you can try to figure out why by [viewing event logs for the stack](#key-tasks-cloudformation-logs)\.

[Top](#key-tasks)

## Working with AWS Lambda Functions<a name="key-tasks-lambda"></a>

After you have [installed the AWS Toolkit for JetBrains](#key-tasks-install) and then used the AWS Toolkit to [connect to an AWS account for the first time](#key-tasks-first-connect), you can use the AWS Toolkit to work with Lambda functions in the account as follows\.
+ [Create a function](#key-tasks-lambda-create)
+ [Run \(invoke\) or debug the local version of a function](#key-tasks-lambda-local)
+ [Run \(invoke\) the remote version of a function](#key-tasks-lambda-remote)
+ [Change \(update\) the configuration for a function](#key-tasks-lambda-update)
+ [Delete a function](#key-tasks-lambda-delete)

[Top](#key-tasks)

### Creating a Function<a name="key-tasks-lambda-create"></a>

You can use the AWS Toolkit to create an AWS Lambda function that is [part of an AWS serverless application](#key-tasks-lambda-create-app), or you can create a Lambda function [by itself](#key-tasks-lambda-create-standalone)\.

#### Creating a Serverless Application that Contains a Lambda Function<a name="key-tasks-lambda-create-app"></a>

See the instructions earlier in this topic about [creating an AWS serverless application](#key-tasks-sam-create)\.

[Top](#key-tasks)

#### Creating a Function by Itself<a name="key-tasks-lambda-create-standalone"></a>

To complete this procedure, you must first [install the AWS Toolkit](#key-tasks-install) and then [connect to an AWS account for the first time](#key-tasks-first-connect), if you have not done so already\. Then, with IntelliJ IDEA or PyCharm already running, do one of the following\.
+ [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](#key-tasks-switch-region) to create the function in if necessary\. Right\-click **Lambda**, and then choose **Create new AWS Lambda**\.  
![\[Choosing to create an AWS Lambda function starting from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

  Complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\. The AWS Toolkit creates a corresponding AWS CloudFormation stack for the deployment and adds the name of the function to the **Lambda** list in the **AWS Explorer**\. If the deployment fails, you can try to figure out why by [viewing event logs for the stack](#key-tasks-cloudformation-logs)\.
+ Create a code file that implements a [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or a [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html)\. 

  To enable running \(invoking\) the remote version of the function, you must also [switch to a different AWS Region](#key-tasks-switch-region) to create the function in if necessary\. Then, in the code file, choose the **Lambda** icon in the gutter next to the function handler, and then choose **Create new AWS Lambda**\. Complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\.  
![\[Choosing to create an AWS Lambda function starting from an existing function handler in a code file\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
**Note**  
If the **Lambda** icon does not display in the gutter next to the function handler, you can try displaying it for the current project by selecting the following box in **Preferences**: **Tools, AWS, Project settings, Show gutter icons for all potential AWS Lambda handlers**\. Also, the **Create new AWS Lambda** command won't display if the function handler is already defined in the corresponding AWS SAM template\.

  After you choose **Create Function**, the AWS Toolkit creates a corresponding function in the Lambda service for the connected AWS account\. If the operation succeeds, after you refresh the **AWS Explorer**, the **Lambda** list displays the name of the new function\.
+ If you already have a project that contains an AWS Lambda function, first [switch to a different AWS Region](#key-tasks-switch-region) to create the function in if necessary\. Then, in the code file that contains the [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or the [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html), choose the **Lambda** icon in the gutter next to the function handler\. Choose **Create new AWS Lambda**, complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\.  
![\[Choosing to create an AWS Lambda function starting from an existing function handler in a code file\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
**Note**  
If the **Lambda** icon does not display in the gutter next to the function handler, you can try displaying it for the current project by selecting the following box in **Preferences**: **Tools, AWS, Project settings, Show gutter icons for all potential AWS Lambda handlers**\. Also, the **Create new AWS Lambda** command won't display if the function handler is already defined in the corresponding AWS SAM template\.

  After you choose **Create Function**, the AWS Toolkit creates a corresponding function in the Lambda service for the connected AWS account\. If the operation succeeds, after you refresh the **AWS Explorer**, the **Lambda** list displays the name of the new function\.

After you create the function, you can [run \(invoke\) or debug the local version of the function](#key-tasks-lambda-local) or [run \(invoke\) the remote version](#key-tasks-lambda-remote)\.

[Top](#key-tasks)

### Running \(Invoking\) or Debugging the Local Version of a Function<a name="key-tasks-lambda-local"></a>

A *local* version of an AWS Lambda function is a function whose source code already exists on your local development computer\.

To complete this procedure, you must first [create the AWS Lambda function](#key-tasks-lambda-create) that you want to run \(invoke\) or debug, if you haven't created it already\.
**Note**  
If you want to run \(invoke\) or debug the local version of an AWS Lambda function, and you want to run \(invoke\) or debug that function locally with any non\-default or optional properties, you must first set those properties in the function's corresponding AWS SAM template file \(for example, in a file named `template.yaml` within the project\)\. For a list of available properties, see [AWS::Serverless::Function](https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md#awsserverlessfunction) in the [awslabs/serverless\-application\-model](https://github.com/awslabs/serverless-application-model/) repository on the GitHub website\.

1. Do one of the following\.
   + In the code file that contains the [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or the [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html), choose the Lambda icon in the gutter next to the function handler\. Choose **Run '\[Local\]'** or **Debug '\[Local\]'**\.   
![\[Choosing to run or debug the local version of a Lambda function starting from the function handler in the code file\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + With the **Project** tool window already open and displaying the project that contains the function, open the project's `template.yaml` file\. Choose the **Run** icon in the gutter next to the function's resource definition, and then choose **Run '\[Local\]'** or **Debug '\[Local\]'**\.  
![\[Choosing to run or debug the local version of a Lambda function starting from the function definition in the AWS SAM template file\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Complete the [Edit configuraton dialog](edit-configuration-dialog.md) box if it displays, and then choose **Run** or **Debug**\. \(If the **Edit configuration** dialog box doesn't display and you want to change the existing configuration, [change its configuration](#key-tasks-lambda-update), and then repeat this procedure from the beginning\. If the configuration details are missing, first expand **Templates, AWS Lambda**, and then choose **Local**; choose **OK**; and then repeat this procedure from the beginning\.\) Results are displayed in the **Run** or **Debug** tool window\. 

[Top](#key-tasks)

### Running \(Invoking\) the Remote Version of a Function<a name="key-tasks-lambda-remote"></a>

A *remote* version of an AWS Lambda function is a function whose source code already exists inside of the Lambda service for an AWS account\.

To complete this procedure, you must first [install the AWS Toolkit](#key-tasks-install) and then [connect to an AWS account for the first time](#key-tasks-first-connect), if you have not done so already\. Then, with IntelliJ IDEA or PyCharm already running, do the following\.

1. [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](#key-tasks-switch-region) that contains the function if necessary\.

1. Expand **Lambda**, and confirm that the name of the function is listed\. If it is listed, skip ahead to step 3 in this procedure\.

   If the name of the function is not listed, [create the Lambda function](#key-tasks-lambda-create) that you want to run \(invoke\), if you have not done so already\. 

   If you created the function as [part of an AWS serverless application](#key-tasks-lambda-create-app), you must also [deploy that application](#key-tasks-sam-deploy)\.

   If you created the function by creating a code file that implements a [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or a [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html), then in the code file, choose the Lambda icon next to the function handler, and then choose **Create new AWS Lambda**\. Complete the [Create Function dialog](create-function-dialog.md) box, and then choose **Create Function**\.

1. With **Lambda** already expanded in the **AWS Explorer**, right\-click the name of the function, and then choose **Run '\[Remote\]'**\.  
![\[Choosing to run the remote version of a Lambda function starting from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Complete the [Edit configuraton dialog](edit-configuration-dialog.md) box if it displays, and then choose **Run**\. \(If the **Edit configuration** dialog box doesn't display and you want to change the existing configuration, [change its configuration](#key-tasks-lambda-update), and then repeat from step 3 in this procedure\. If the configuration details are missing, first expand **Templates, AWS Lambda**, and then choose **Remote**; choose **OK**; and then repeat this procedure from the beginning\.\) Results are displayed in the **Run** tool window\. 

[Top](#key-tasks)

### Changing \(Updating\) the Configuration for a Function<a name="key-tasks-lambda-update"></a>

Do one of the following\.
+ With the code file open that contains the [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or the [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html), on the main menu, choose **Run, Edit Configurations**\. Complete the [Run/Debug Configurations dialog](run-debug-configurations-dialog.md) box, and then choose **OK**\.
+ [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](#key-tasks-switch-region) that contains the function if necessary\. Expand **Lambda**, choose the name of the function that you want to change the configuration for, and then do one of the following\.
  + To change settings such as the timeout, memory, environment variables, and execution role: right\-click the name of the function, and then choose **Update Function Configuration**\.  
![\[Choosing the Update Function Configuration command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

    Complete the [Update Configuration dialog](update-configuration-dialog.md) box, and then choose **Update**\. 
  + To change settings such as the input payload: on the main menu, choose **Run, Edit Configurations**\. Complete the [Run/Debug Configurations dialog](run-debug-configurations-dialog.md) box, and choose **OK**\.  
![\[Choosing the Edit Configurations command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

    \(If the configuration details are missing, first expand **Templates, AWS Lambda**, and then choose **Local** \(for the local version of the function\) or **Remote** \(for the remote version of that same function\); choose **OK**; and then repeat this procedure from the beginning\.\)
  + To change settings such as the function handler name or Amazon S3 source bucket: right\-click the name of the function, and then choose **Update Function Code**\.  
![\[Choosing the Update Function Code command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

    Complete the [Update Code dialog](update-code-dialog.md) box, and then choose **Update**\.
  + To change any other available property settings that are not listed in the preceding bullets, change those settings in the function's corresponding AWS SAM template file \(for example, in a file named `template.yaml` within the project\)\. For a list of available property settings, see [AWS::Serverless::Function](https://github.com/awslabs/serverless-application-model/blob/master/versions/2016-10-31.md#awsserverlessfunction) in the [awslabs/serverless\-application\-model](https://github.com/awslabs/serverless-application-model/) repository on the GitHub website\. 

[Top](#key-tasks)

### Deleting a Function<a name="key-tasks-lambda-delete"></a>

You can use the AWS Toolkit to delete an AWS Lambda function that is [part of an AWS serverless application](#key-tasks-lambda-delete-sam), or you can delete a Lambda function that exists [by itself](#key-tasks-lambda-delete-standalone)\.

#### Deleting a Serverless Application that Contains a Function<a name="key-tasks-lambda-delete-sam"></a>

See the instructions earlier in this topic about [deleting a serverless application](#key-tasks-sam-delete)\.

[Top](#key-tasks)

#### Deleting a Function that Exists by Itself<a name="key-tasks-lambda-delete-standalone"></a>

1. [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](#key-tasks-switch-region) that contains the function if necessary\.

1. Expand **Lambda**\.

1. Right\-click the name of the function to delete, and then choose **Delete Function**\.  
![\[Choosing the Delete Function command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Type the function's name to confirm the deletion, and then choose **OK**\. If the function deletion is successful, the AWS Toolkit removes the name of the function from the **Lambda** list\.

[Top](#key-tasks)

## Working with AWS CloudFormation Stacks<a name="key-tasks-cloudformation"></a>

After you have [installed the AWS Toolkit for JetBrains](#key-tasks-install) and then used the AWS Toolkit to [connect to an AWS account for the first time](#key-tasks-first-connect), you can use the AWS Toolkit to work with AWS CloudFormation stacks in the account as follows\.
+ [View event logs for a stack](#key-tasks-cloudformation-logs)
+ [Delete a stack](#key-tasks-cloudformation-delete)

Currently you cannot use the AWS Toolkit to directly [create stacks](#key-tasks-cloudformation-create) or to [change stack settings](#key-tasks-cloudformation-change)\. However, you can do these indirectly as part of working with AWS serverless applications and AWS Lambda functions, as follows\.

[Top](#key-tasks)

### Creating a Stack<a name="key-tasks-cloudformation-create"></a>

Currently, you cannot use the AWS Toolkit to create an AWS CloudFormation stack directly\. However, whenever you use the AWS Toolkit to [deploy an AWS serverless application](#key-tasks-sam-deploy) or to [create and then deploy an AWS Lambda function](#key-tasks-lambda-create-standalone), the AWS Toolkit deploys these by first creating a corresponding stack in AWS CloudFormation and then using that stack for the deployment\.

[Top](#key-tasks)

### Changing Stack Settings<a name="key-tasks-cloudformation-change"></a>

Currently you cannot use the AWS Toolkit to change the settings for an AWS CloudFormation stack directly\. However, you can [change \(update\) the settings for an AWS serverless application](#key-tasks-sam-update) that belongs to a stack, or [change \(update\) the configuration for an AWS Lambda function](#key-tasks-lambda-update) that belongs to a stack, and then [deploy that serverless application](#key-tasks-sam-deploy) again or deploy that function \(as part of the lifecycle of [running \(invoking\) the remote version of that function](#key-tasks-lambda-remote)\) again\. 

[Top](#key-tasks)

### Viewing Event Logs for a Stack<a name="key-tasks-cloudformation-logs"></a>

1. [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](#key-tasks-switch-region) that contains the stack if necessary\.

1. Expand **CloudFormation**\.

1. Double\-click the name of the stack to view event logs for\. The AWS Toolkit displays the event logs in the **CloudFormation** tool window\.  
![\[Choosing to view event logs for an AWS CloudFormation stack starting from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

   \(To hide or show the **CloudFormation** tool window, on the main menu, choose **View, Tool Windows, CloudFormation**\.\)

[Top](#key-tasks)

### Deleting a Stack<a name="key-tasks-cloudformation-delete"></a>

1. [Open the AWS Explorer](#key-tasks-open-explorer), if it is not already open, [switching to a different AWS Region](#key-tasks-switch-region) that contains the stack if necessary\.

1. Expand **CloudFormation**\.

1. Right\-click the name of the stack to delete, and then choose **Delete CloudFormation Stack**\.  
![\[Choosing to delete a AWS CloudFormation stack starting from the AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Type the stack's name to confirm the deletion, and then choose **OK**\. If the stack deletion is successful, the AWS Toolkit removes the name of the stack from the **CloudFormation** list in the **AWS Explorer**\. If the stack deletion fails, you can try to figure out why by [viewing the event logs for the stack](#key-tasks-cloudformation-logs)\.

[Top](#key-tasks)