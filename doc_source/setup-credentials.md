# Setting AWS credentials for the AWS Toolkit for JetBrains<a name="setup-credentials"></a>

To access an AWS account by using the AWS Toolkit for JetBrains, you must first connect the toolkit to that account\. There are two options for connecting to your account:
+ Add access keys to specify the AWS credentials for the account\.
+ Add a named profile for the account that will be logged in using AWS Single Sign\-On \([AWS SSO](https://docs.aws.amazon.com/singlesignon/latest/userguide/)\)\.

Complete the following procedures to make an initial connection, switch between connections, change connections, delete connections, and more\.

**Topics**
+ [Accessing credentials files](#setup-credentials-first-connect)
+ [Getting the current connection](#setup-credentials-current-connect)
+ [Adding multiple connections](#setup-credentials-multiple-connect)
+ [Switching between connections](#setup-credentials-switch-connect)
+ [Changing connection settings](#setup-credentials-change-connect)
+ [Deleting a connection](#setup-credentials-delete-connect)

## Accessing credentials files<a name="setup-credentials-first-connect"></a>

You should have already [installed the AWS Toolkit for JetBrains](key-tasks.md#key-tasks-install)\. Depending on your connection option, you must have completed the following prerequisites:
+ AWS security credentials—Created an [access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) \(which contains both an *access key ID* value and a *secret access key* value\) for a user in IAM \(which we recommend\), or an AWS account root user \(which we strongly discourage\)\. If you don't have an access key for a user in IAM, [create one](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey)\.
+ AWS SSO—Configured single sign\-on by enabling AWS SSO, managing your identity source, and assigning SSO access to AWS accounts\. For more information about this process, see the [Getting started](AWS Single Sign-On User Guidegetting-started.html) chapter of the *AWS Single Sign\-On User Guide*\.
**Note**  
We recommend storing sensitive credential information, such as named profiles that include access keys, in the `credentials` file\. Less sensitive configuration options, such as named profiles that use AWS SSO for authentication, are normally stored in the `config` file\.  
You can store all your named profiles in a single file\. If you're using both `credentials` and `config` files, `credentials` is opened by default in the IDE\.   
If there are credentials in both files for a profile sharing the same name, the keys in the `credentials` file take precedence\. For more information, see [Configuration and credential file settings](AWS Command Line Interface User Guidecli-configure-files.html) in the *AWS Command Line Interface User Guide*\. 
+ To open the credentials for editing, do one of the following:
  + On the status bar, choose **AWS: No credentials selected**, and then choose **Edit AWS Credential file\(s\)**\.  
![\[AWS no credentials selected on the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)  
![\[Edit AWS credentials from the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
  + [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open\. Choose **Configure AWS Connection**, and then choose **Edit AWS Credential file\(s\)**\.  
![\[Configure AWS connection from AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)  
![\[Edit AWS credentials from AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

After you open the credentials file, you can edit it to specify access to your AWS account using access keys or AWS SSO\.

------
#### [  Connect with access keys  ]

1. In the file, under `[default]`, for `aws_access_key_id`, replace `[accessKey1]` with your access key ID value \(for example, `AKIAIOSFODNN7EXAMPLE`\)\.

   If prompted, choose **I want to edit this file anyway**, and then choose **OK**\.

1. For `aws_secret_access_key`, replace `[secretKey1]` with your secret access key value \(for example, `wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY`\)\.

   The final results should look as shown here, following the [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) format\.

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
The AWS Toolkit for JetBrains currently supports the following configuration variables:  
`aws_access_key_id`
`aws_secret_access_key`
`aws_session_token`
`credential_process`
`external_id`
`mfa_serial`
`role_arn`
`source_profile`
For more information, see [AWS CLI configuration variables](https://docs.aws.amazon.com/cli/latest/topic/config-vars.html) in the *AWS CLI Command Reference*\.

1. Save and then close the file\. The AWS Toolkit for JetBrains tries to connect to the account by using the preceding access key\. 

   After connecting, you can use the toolkit to work with AWS resources in that account, such as [AWS serverless](key-tasks.md#key-tasks-sam) applications, [AWS Lambda](key-tasks.md#key-tasks-lambda) functions, and [AWS CloudFormation](key-tasks.md#key-tasks-cloudformation) stacks\.

------
#### [ Connect with AWS SSO ]<a name="SSO-profile"></a>

With AWS SSO, you define a named profile in the `credentials` file or `config` that you use to retrieve temporary credentials for your AWS account\. The profile definition specifies the SSO user portal as well as the AWS account and IAM role associated with the user requesting access\.

AWS Toolkit for JetBrains calls the AWS CLI `login` command on your behalf\. \(The named profile that you added is passed as an option to `login`\)\. If the login is successful, your default browser is launched and verifies your AWS SSO login\. You can then start accessing the AWS resources available in your account\.

1. In the `credentials`/`config` file, under `[default]`, add a template for a named profile\. 

   You can use an example like the one that follows as a template for a typical AWS SSO profile\.
**Important**  
For named profiles, the `credentials` file uses a different naming format than the `config` file\. Include the prefix word `profile` only when configuring a named profile in the `config` file\. Do **not** use the word `profile` when creating an entry in the `credentials` file\.

   ```
   ... Named profile in credentials file ...
   
   [default]
   sso_start_url = https://my-sso-portal.awsapps.com/start
   sso_region = us-east-1
   sso_account_id = 123456789011
   sso_role_name = readOnly
   region = us-west-2
   
   ... Named profile in config file ...
   
   [profile user1]
   sso_start_url = https://my-sso-portal.awsapps.com/start
   sso_region = us-east-1
   sso_account_id = 123456789011
   sso_role_name = readOnly
   region = us-west-2
   
   ... Other file contents omitted for brevity ...
   ```

1. Assign values to the keys that are specific to your SSO configuration:
   + `sso_start_url` – Specifies the URL that points to the organization's AWS SSO user portal\.
   + `sso_region` – Specifies the AWS Region that contains the AWS SSO portal host\. This is separate from and can be a different AWS Region than that specified by the default `region` parameter\.
   + `sso_account_id` – Specifies the AWS account ID that contains the IAM role with the permission that you want to grant to the associated AWS SSO user\.
   + `sso_role_name` – Specifies the friendly name of the IAM role that defines the user's permissions when using this profile to get credentials through AWS SSO\.
   + `region` IAM Specifies the AWS Region that contains the AWS SSO portal host\. This is separate from and can be a different AWS Region than that specified by the default `region` parameter\. 
**Note**  
You can also include any other keys and values that are valid in the `.aws/credentials file`, such as `output` or `S3`\. However, you can't include any credential\-related values, such as `role_arn` or `aws_secret_access_key`\. If you do, the AWS CLI produces an error\.  
For more information, see [Configuring the AWS CLI to use AWS Single Sign\-On](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-sso.html#sso-configure-profile) in the *AWS Command Line Interface User Guide*\.

   After AWS Toolkit for JetBrains calls the AWS SSO `login` command on your behalf, a browser window launches to confirm the SSO login was successful\.

------

You can also have [more than one connection](key-tasks.md#key-tasks-multiple-connect) available, so that you can [switch between them](key-tasks.md#key-tasks-switch-connect)\.

After you connect, the AWS Toolkit for JetBrains selects the default AWS Region automatically\. You might need to [switch to working with different AWS resources that are in a different Region](key-tasks.md#key-tasks-switch-region)\.

## Getting the current connection<a name="setup-credentials-current-connect"></a>

To check which connection the AWS Toolkit for JetBrains is currently using, do one of the following:
+ On the status bar, see the current connection displayed in the **AWS Connection Settings** area\.  
![\[The current connection in the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
+ [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it's not already open, and then choose **Show Options Menu** \(the settings icon\)\. Choose **AWS Connection Settings**\. The current connection is selected\.  
![\[The current connection in AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

You can also have [more than one connection](key-tasks.md#key-tasks-multiple-connect) available, so that you can [switch between them](key-tasks.md#key-tasks-switch-connect)\.

## Adding multiple connections<a name="setup-credentials-multiple-connect"></a>

Depending on the additional connection you want to add, you must first have completed one of the following tasks:
+ Created an additional [access key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) \(which contains both an *access key ID* value and a *secret access key* value\) for a user in IAM \(which we recommend\) or AWS account root user \(which we strongly discourage\)\. If you don't have an access key for a user IAM already, [create one](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey)\.
+ Enabled [AWS SSO access](AWS Single Sign-On User Guidegetting-started.html) for the additional user's AWS account\.
**Note**  
We recommend storing sensitive credential information, such as named profiles that include access keys, in the `credentials` file\. Less sensitive configuration options, such as named profiles that use AWS SSO for authentication, are normally stored in the `config` file\.  
You can store all your named profiles in a single file\. If you're using both `credentials` and `config` files, `credentials` is opened by default in the IDE\.   
If there are credentials in both files for a profile sharing the same name, the keys in the `credentials` file take precedence\. For more information, see [Configuration and credential file settings](AWS Command Line Interface User Guidecli-configure-files.html) in the *AWS Command Line Interface User Guide*\. 

1. [Connect for the first time](key-tasks.md#key-tasks-first-connect), if you have not done so already\.

1. To start editing the credentials file, do one of the following:
   + On the status bar, choose **AWS Connection Settings**, and then choose **All Credentials**, **Edit AWS Credential file\(s\)**\.  
![\[Choosing to edit AWS credentials from the status bar\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open, and then choose **Show Options Menu** \(the settings icon\)\. Choose **AWS Connection Settings**, **All Credentials**, **Edit AWS Credential file\(s\)**\.  
![\[Choosing to edit AWS credentials from AWS Explorer\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. In the file, add a [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) for each additional connection\. Profile names can contain only the uppercase letters  **A** through **Z**, the lowercase letters **a** through **z**, the numbers **0** through **9**, the hyphen character \( **\-**\), and the underscore character \( **\_**\)\. Profile names must be less than 64 characters in length\. 

------
#### [  Profile with access keys  ]

   For example, for a named profile named `myuser`, use the following format\.

   ```
   [myuser]
   aws_access_key_id = AKIAIOSFODNN7EXAMPLE
   aws_secret_access_key = wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
   ```

**Note**  
The AWS Toolkit for JetBrains currently supports named profiles with only the following characters: **A**\-**Z**, **a**\-**z**, **0**\-**9**, underscore \(**\_**\), and hyphen \(**\-**\)\.  
Currently, the toolkit supports only the following configuration variables:  
`aws_access_key_id`
`aws_secret_access_key`
`aws_session_token`
`credential_process`
`mfa_serial`
`role_arn`
`source_profile`
For more information, see [AWS CLI configuration variables](https://docs.aws.amazon.com/cli/latest/topic/config-vars.html) in the *AWS CLI Command Reference*\.

------
#### [  Profile with AWS SSO ]

   With AWS SSO, you can enable multiple connections by adding named profiles that define how specific accounts are authenticated using single sign\-on\. Ensure each named profile that you add to the `credentials` file has a unique name and assign account\-specific values to the SSO keys\. This is shown in the following example\.

   ```
   ... Other file contents omitted for brevity ...
   
   [profile user2]
   sso_start_url = https://my-sso-portal.awsapps.com/start
   sso_region = us-east-1
   sso_account_id = 123456789011
   sso_role_name = readOnly
   region = us-west-2
   
   
   ... Other file contents omitted for brevity ...
   ```

   For more information about the AWS SSO key\-value pairs, see [defining named profiles for SSO](#SSO-profile)\.

------

1. Save and then close the file\. The AWS Toolkit for JetBrains displays the new connection in the **AWS Connection Settings** menu in both the status bar and in **AWS Explorer**\.

Now that you have multiple connections, you can [switch between them](key-tasks.md#key-tasks-switch-connect), if you want\.

After you connect, you might need to [switch to working with AWS resources in that account that are in a different AWS Region](key-tasks.md#key-tasks-switch-region)\.

## Switching between connections<a name="setup-credentials-switch-connect"></a>

1. [Add multiple connections](key-tasks.md#key-tasks-multiple-connect), if you haven't done so already\.

1. Do one of the following:
   + On the status bar, choose **AWS Connection Settings**\.
   + [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open, and then choose **AWS Connection Settings**\.

1. Choose the [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) to use for the new connection\. If it isn't listed, choose **All Credentials**, and then choose the [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) to use\.   
![\[Switching the current connection\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

   The AWS Toolkit for JetBrains switches to the new connection\. This connection is now selected in the **AWS Connection Settings** menu in both the status bar and **AWS Explorer**\.

After you connect, you might need to [switch to working with AWS resources in that account that are in a different AWS Region](key-tasks.md#key-tasks-switch-region)\.

## Changing connection settings<a name="setup-credentials-change-connect"></a>

1. Do one of the following:
   + On the status bar, choose **AWS Connection Settings**, **All Credentials**, **Edit AWS Credential file\(s\)**\.  
![\[Choosing the Edit AWS Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open, and then choose **Show Options Menu** \(the settings icon\)\. Then choose **AWS Connection Settings**, **All Credentials**, **Edit AWS Credential file\(s\)**\.  
![\[Choosing the Edit AWS Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. Make your changes to the file, and then save and close the file\. 

## Deleting a connection<a name="setup-credentials-delete-connect"></a>

1. Do one of the following:
   + On the status bar, choose **AWS Connection Settings**, **All Credentials**, **Edit AWS Credential file\(s\)**\.  
![\[Choosing the Edit AWS Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
   + [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open, and then choose **Show Options Menu** \(the settings icon\)\. Then choose **AWS Connection Settings**, **All Credentials**, **Edit AWS Credential file\(s\)**\.  
![\[Choosing the Edit AWS Credential files command\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

1. In the file, completely delete the [named profile](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) \(specifying access keys or AWS SSO key\-value pairs\) for the connection that you want to delete\.

1. Save and then close the file\. The AWS Toolkit for JetBrains removes the deleted connection from the **AWS Connection Settings** menu in both the status bar and in **AWS Explorer**\.

After you delete a connection, you might need to [switch to a different connection](key-tasks.md#key-tasks-switch-connect) or [connect for the first time](key-tasks.md#key-tasks-first-connect) again\.