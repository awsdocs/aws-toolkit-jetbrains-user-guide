# New Project dialog box<a name="new-project-dialog"></a>

The **New Project** dialog box in the AWS Toolkit for JetBrains is displayed when you [create an AWS serverless application](key-tasks.md#key-tasks-sam-create)\.

**Topics**
+ [New Project dialog box \(IntelliJ IDEA, PyCharm, and WebStorm\)](#new-project-dialog-intellij)
+ [New Project dialog box \(JetBrains Rider\)](#new-project-dialog-rider)

## New Project dialog box \(IntelliJ IDEA, PyCharm, and WebStorm\)<a name="new-project-dialog-intellij"></a>

**Note**  
The following screenshot shows the **New Project** dialog box for IntelliJ IDEA, but the field descriptions also apply to PyCharm and WebStorm\.

![\[The New Project dialog box for IntelliJ IDEA.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **New Project** dialog box contains the following items:

**Project name**  
\(Required\) The name of the project\.

**Project location**  
\(Required\) The location where IntelliJ IDEA creates the project\.

**Package Type**  
\(Required\) The AWS Lambda function's deployment package type, which can be either `Zip` or `Image`\. For information about the difference between `Zip` and `Image` package types, see [Lambda deployment packages](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html) in the *AWS Lambda Developer Guide*\.

**Runtime**  
\(Required\) The ID of the [Lambda runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) to use\.

**SAM Template**  
\(Required\) The name of the AWS Serverless Application Model \(AWS SAM\) template to use\.

**Project SDK**  
\(Required\) The Java development kit \(JDK\) to use\. For more information, see [Java Development Kit \(JDK\)](https://www.jetbrains.com/help/idea/sdk.html#jdk) on the IntelliJ IDEA Help website\.

## New Project dialog box \(JetBrains Rider\)<a name="new-project-dialog-rider"></a>

**Note**  
When you create a new solution, this dialog box contains the title **New Solution** instead of **New Project**\. However, the dialog box's contents are the same\.

![\[The New Project dialog box for JetBrains Rider.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **New Project** dialog box contains the following items:

**Solution name**  
\(Required\) The name of the solution\.

**Project name**  
\(Required\) The name of the project\.

**Solution directory**  
\(Required\) The path to the solution's directory\.

**Put solution and project in the same directory**  
\(Optional\) If selected, puts the solution's files in the same location as the project's files\.

**Create repository**  
\(Optional\) If selected, creates a remote repository for the project with the specified provider\.

**Package Type**  
\(Required\) The Lambda function's package type, which can be either `Zip` or `Image`\. For information about the difference between `Zip` and `Image` package types, see [Lambda deployment packages](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html) in the *AWS Lambda Developer Guide*\.

**Runtime**  
\(Required\) The ID of the Lambda runtime to use\.

**SAM Template**  
\(Required\) The name of the AWS SAM template to use\.

**Resulting project structure**  
\(Non\-editable\) The paths for the created project's directories and files\.
