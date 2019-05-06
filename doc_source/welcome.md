# What Is the AWS Toolkit for JetBrains?<a name="welcome"></a>


|  | 
| --- |
| If you just want to start using the AWS Toolkit for JetBrains right away, then skip ahead to the [installation](key-tasks.md#key-tasks-install) and [first\-time connection](key-tasks.md#key-tasks-first-connect) instructions\.  | 

The AWS Toolkit for JetBrains \(which covers both the [AWS Toolkit for IntelliJ](https://aws.amazon.com/intellij/) and the [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/)\) is an open source plug\-in for the integrated development environments \(IDEs\) from JetBrains that makes it easier for developers to develop, debug, and deploy serverless applications that use Amazon Web Services \(AWS\)\. You can also use the AWS Toolkit to work with AWS Lambda functions and AWS CloudFormation stacks\. The AWS Toolkit includes features like AWS credentials management and AWS Region management that simplify writing applications for AWS\.

![\[The AWS Toolkit in IntelliJ IDEA\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

![\[The AWS Toolkit in PyCharm\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The AWS Toolkit for JetBrains covers both the [AWS Toolkit for IntelliJ](https://aws.amazon.com/intellij/) \(for Java development\) and the [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) \(for Python development\)\. When there are differences in functionality between these two products, this *User Guide* will note them accordingly\.

**Topics**
+ [How Do I Get Started?](#welcome-)
+ [What Can I Do with the AWS Toolkit?](#welcome-using)
+ [Related Videos](#welcome-videos)
+ [Related Web Pages](#welcome-help)
+ [I Have Questions or Need Help](#welcome-help)
+ [I Want to Report a Bug with the AWS Toolkit or Make a Feature Request](#welcome-issues)
+ [I Want to Contribute to the AWS Toolkit](#welcome-contribute)

## How Do I Get Started?<a name="welcome-"></a>

To begin using the AWS Toolkit for JetBrains, follow the [installation](key-tasks.md#key-tasks-install) and [first\-time connection](key-tasks.md#key-tasks-first-connect) instructions\.

After you install the AWS Toolkit and connect it to an AWS account, you can use the AWS Toolkit to work with [AWS serverless applications](key-tasks.md#key-tasks-sam), [AWS Lambda functions](key-tasks.md#key-tasks-lambda), and [AWS CloudFormation stacks](key-tasks.md#key-tasks-cloudformation) in that account\.

For brief instructions about how to use other available AWS Toolkit features, see the [key tasks](key-tasks.md)\.

## What Can I Do with the AWS Toolkit?<a name="welcome-using"></a>
+ [Create](key-tasks.md#key-tasks-sam-create), [deploy](key-tasks.md#key-tasks-sam-deploy), [change](key-tasks.md#key-tasks-sam-update), and [delete](key-tasks.md#key-tasks-sam-delete) [AWS serverless](https://aws.amazon.com/serverless/) applications in an AWS account\.
+ [Create](key-tasks.md#key-tasks-lambda-create), [run \(invoke\) and debug locally](key-tasks.md#key-tasks-lambda-local), [run \(invoke\) remotely](key-tasks.md#key-tasks-lambda-remote), [change](key-tasks.md#key-tasks-lambda-update), and [delete](key-tasks.md#key-tasks-lambda-delete) [AWS Lambda](https://aws.amazon.com/lambda/) functions in an AWS account\.
+ [View event logs](key-tasks.md#key-tasks-cloudformation-logs) for and [delete](key-tasks.md#key-tasks-cloudformation-delete) [AWS CloudFormation](https://aws.amazon.com/cloudformation/) stacks in an AWS account\.
+ [Switch to using different AWS credentials to connect with a different set of access permissions within the same AWS account or a different one](key-tasks.md#key-tasks-switch-connect)\.
+ [Switch to working with AWS resources in a different AWS Region for the connected AWS account](key-tasks.md#key-tasks-switch-region)\.
+ [Use an HTTP proxy](key-tasks.md#key-tasks-proxy) and [update it](key-tasks.md#key-tasks-update) as needed\.

## Related Videos<a name="welcome-videos"></a>
+ [Announcement \| Introducing the AWS Toolkit for IntelliJ IDEA](https://www.youtube.com/watch?v=xbbkNVr27Is) \(16 minutes, April 2019, YouTube website\)
+ [Getting Started with the AWS Toolkit for JetBrains](https://www.youtube.com/watch?v=oHge7MytYv4) \(covers the AWS Toolkit for PyCharm only\) \(2 minutes, November 2018, YouTube website\)
+ [Building Serverless Applications with the AWS Toolkit for JetBrains](https://www.youtube.com/watch?v=kyZpAnDc4Qs) \(covers the AWS Toolkit for PyCharm only\) \(6 minutes, November 2018, YouTube website\)

## Related Web Pages<a name="welcome-help"></a>
+ [The AWS Toolkit for IntelliJ is Now Generally Available](https://aws.amazon.com/about-aws/whats-new/2019/03/the-aws-toolkit-for-intellij-is-now-generally-available/) post \(March 2019, AWS website\)
+ [AWS Toolkit for IntelliJ – Now generally available](https://aws.amazon.com/blogs/developer/aws-toolkit-for-intellij-now-generally-available/) blog post \(March 2019, AWS website\)
+ [New – AWS Toolkits for PyCharm, IntelliJ \(Preview\)](https://aws.amazon.com/blogs/aws/new-aws-toolkits-for-pycharm-intellij-preview-and-visual-studio-code-preview/) blog post \(November 2018, AWS website\)
+ [Introducing the AWS Toolkit for PyCharm](https://aws.amazon.com/about-aws/whats-new/2018/11/introducing-aws-toolkit-for-pycharm/) post \(November 2018, AWS website\)
+ To learn more about the AWS Toolkit for IntelliJ \(which is part of the AWS Toolkit for JetBrains\), see [AWS Toolkit for IntelliJ](https://aws.amazon.com/intellij/) on the AWS website\.
+ To learn more about the AWS Toolkit for PyCharm \(which is part of the AWS Toolkit for JetBrains\), see [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) on the AWS website\.
+ To learn more about the AWS Toolkit, see [AWS Toolkit](https://plugins.jetbrains.com/plugin/11349-aws-toolkit) on the JetBrains website\.
+ To learn more about developing on AWS with JetBrains, see [Develop on AWS with JetBrains Tools](https://www.jetbrains.com/devops/amazon-aws/) on the JetBrains website\.
+ To learn more about JetBrains, see [All Developer Tools and Products by JetBrains](https://www.jetbrains.com/products.html) on the JetBrains website\.

## I Have Questions or Need Help<a name="welcome-help"></a>

To ask questions or seek help from the AWS developer community, see the [Java Development Discussion Forum](https://forums.aws.amazon.com/forum.jspa?forumID=70) or the [Python Development Discussion Forum](https://forums.aws.amazon.com/forum.jspa?forumID=132) on the AWS website\. \(When you enter these forums, AWS might require you to sign in\.\) 

You can also [contact us](https://aws.amazon.com/contact-us/) directly\. 

## I Want to Report a Bug with the AWS Toolkit or Make a Feature Request<a name="welcome-issues"></a>

To report a bug with the AWS Toolkit for JetBrains or to make a feature request, go to the [Issues](https://github.com/aws/aws-toolkit-jetbrains/issues) tab in the [aws/aws\-toolkit\-jetbrains](https://github.com/aws/aws-toolkit-jetbrains) repository on the GitHub website, choose **New issue**, and then follow the on\-screen instructions to finish making your bug report or feature request\. \(When you enter this website, GitHub might require you to sign in\.\)

## I Want to Contribute to the AWS Toolkit<a name="welcome-contribute"></a>

We greatly value your contributions to the AWS Toolkit\. To begin contributing, read the [Contributing Guidelines](https://github.com/aws/aws-toolkit-jetbrains/blob/master/CONTRIBUTING.md) in the [aws/aws\-toolkit\-jetbrains](https://github.com/aws/aws-toolkit-jetbrains) repository on the GitHub website\. \(When you enter this website, GitHub might require you to sign in\.\)