# What Is the AWS Toolkit for JetBrains?<a name="welcome"></a>


|  | 
| --- |
|  To start using the AWS Toolkit for JetBrains right away, skip ahead to the [installation](key-tasks.md#key-tasks-install) and [first\-time connection](key-tasks.md#key-tasks-first-connect) instructions\.  | 

The AWS Toolkit for JetBrains is an open source plugin for the integrated development environments \(IDEs\) from JetBrains\. The toolkit makes it easier for developers to develop, debug, and deploy serverless applications that use Amazon Web Services \(AWS\)\. 

The AWS Toolkit for JetBrains includes the following:
+  The [AWS Toolkit for IntelliJ](https://aws.amazon.com/intellij/) \(for Java development\)\.
+ The [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) \(for Python development\)\.
+ The [AWS Toolkit for WebStorm](https://aws.amazon.com/webstorm/) \(for Node\.js development\)\. 
+ The [AWS Toolkit for Rider](https://aws.amazon.com/rider/) \(for \.NET development\)\. 

**Note**  
When there are differences in functionality between the AWS Toolkit for IntelliJ, the AWS Toolkit for PyCharm, the AWS Toolkit for WebStorm, and the AWS Toolkit for Rider, we note them in this User Guide\.

You can also use the AWS Toolkit for JetBrains to work with AWS Lambda functions, AWS CloudFormation stacks, and Amazon ECS clusters\. The AWS Toolkit for JetBrains includes features such as AWS credentials management and AWS Region management, which simplify writing applications for AWS\.

![\[The AWS Toolkit for JetBrains in IntelliJ IDEA\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

![\[The AWS Toolkit for JetBrains in PyCharm\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

![\[The AWS Toolkit for JetBrains in WebStorm\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

![\[The AWS Toolkit for JetBrains in JetBrains Rider\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

**Topics**
+ [How to Get Started](#welcome-)
+ [What You Can Do with the AWS Toolkit for JetBrains](#welcome-using)
+ [Related Information](#welcome-related)

## How to Get Started<a name="welcome-"></a>

To start using the AWS Toolkit for JetBrains, follow the [installation](key-tasks.md#key-tasks-install) and [first\-time connection](key-tasks.md#key-tasks-first-connect) instructions\.

After you install the AWS Toolkit and connect it to an AWS account, you can use it to work with [AWS serverless applications](key-tasks.md#key-tasks-sam), [AWS Lambda functions](key-tasks.md#key-tasks-lambda), [AWS CloudFormation stacks](key-tasks.md#key-tasks-cloudformation), and [Amazon ECS clusters](key-tasks.md#key-tasks-ecs) in that account\.

For brief instructions about how to use other available AWS Toolkit features, see the [key tasks](key-tasks.md)\.

## What You Can Do with the AWS Toolkit for JetBrains<a name="welcome-using"></a>

You can use the AWS Toolkit for JetBrains to:
+ [Create](key-tasks.md#key-tasks-sam-create), [deploy](key-tasks.md#key-tasks-sam-deploy), [change](key-tasks.md#key-tasks-sam-update), and [delete](key-tasks.md#key-tasks-sam-delete) [AWS serverless](https://aws.amazon.com/serverless/) applications in an AWS account\.
+ [Create](key-tasks.md#key-tasks-lambda-create), [run \(invoke\) and debug locally](key-tasks.md#key-tasks-lambda-local), [run \(invoke\) remotely](key-tasks.md#key-tasks-lambda-remote), [change](key-tasks.md#key-tasks-lambda-update), and [delete](key-tasks.md#key-tasks-lambda-delete) [AWS Lambda](https://aws.amazon.com/lambda/) functions in an AWS account\.
+ [View event logs](key-tasks.md#key-tasks-cloudformation-logs) for and [delete](key-tasks.md#key-tasks-cloudformation-delete) [AWS CloudFormation](https://aws.amazon.com/cloudformation/) stacks in an AWS account\.
+ Debug code in [Amazon ECS](key-tasks.md#key-tasks-ecs-debug) clusters in an AWS account\. \(Debugging code in Amazon ECS clusters is currently in beta\.\)
+ Work with [Amazon EventBridge](key-tasks.md#key-tasks-eventbridge) schemas in an AWS account\.
+ [Switch to using different AWS credentials to connect with a different set of access permissions within the same AWS account or a different one](key-tasks.md#key-tasks-switch-connect)\.
+ [Switch to working with AWS resources in a different AWS Region for the connected AWS account](key-tasks.md#key-tasks-switch-region)\.
+ [Use an HTTP proxy](key-tasks.md#key-tasks-proxy) and [update it](key-tasks.md#key-tasks-update) as needed\.

## Related Information<a name="welcome-related"></a>

### Related Videos<a name="welcome-videos"></a>
+ [Announcement \| Introducing the AWS Toolkit for IntelliJ IDEA](https://www.youtube.com/watch?v=xbbkNVr27Is) \(16 minutes, April 2019, YouTube website\)
+ [Getting Started with the AWS Toolkit for JetBrains](https://www.youtube.com/watch?v=oHge7MytYv4) \(covers the AWS Toolkit for PyCharm only, 2 minutes, November 2018, YouTube website\)
+ [Building Serverless Applications with the AWS Toolkit for JetBrains](https://www.youtube.com/watch?v=kyZpAnDc4Qs) \(covers the AWS Toolkit for PyCharm only, 6 minutes, November 2018, YouTube website\)

### Related Webpages<a name="welcome-help"></a>
+ [The AWS Toolkit for IntelliJ is Now Generally Available](https://aws.amazon.com/about-aws/whats-new/2019/03/the-aws-toolkit-for-intellij-is-now-generally-available/) \(March 2019, blog post, AWS website\)
+ [AWS Toolkit for IntelliJ – Now generally available](https://aws.amazon.com/blogs/developer/aws-toolkit-for-intellij-now-generally-available/) \(March 2019, blog post, AWS website\)
+ [New – AWS Toolkits for PyCharm, IntelliJ \(Preview\)](https://aws.amazon.com/blogs/aws/new-aws-toolkits-for-pycharm-intellij-preview-and-visual-studio-code-preview/) \(November 2018, blog post, AWS website\)
+ [Introducing the AWS Toolkit for PyCharm](https://aws.amazon.com/about-aws/whats-new/2018/11/introducing-aws-toolkit-for-pycharm/) \(November 2018, blog post, AWS website\)
+ [AWS Toolkit for IntelliJ](https://aws.amazon.com/intellij/) \(part of the AWS Toolkit for JetBrains, AWS website\)
+ [AWS Toolkit for PyCharm](https://aws.amazon.com/pycharm/) \(part of the AWS Toolkit for JetBrains, AWS website\)
+ [AWS Toolkit](https://plugins.jetbrains.com/plugin/11349-aws-toolkit) \(JetBrains website\)
+ [Develop on AWS with JetBrains Tools](https://www.jetbrains.com/devops/amazon-aws/) \(JetBrains website\)
+ [All Developer Tools and Products by JetBrains](https://www.jetbrains.com/products.html) \(JetBrains website\)

### Questions and Help<a name="welcome-help"></a>

To ask questions or seek help from the AWS developer community, see the following AWS Discussion Forums:
+ [Java Development](https://forums.aws.amazon.com/forum.jspa?forumID=70)
+ [Python Development](https://forums.aws.amazon.com/forum.jspa?forumID=132)
+ [JavaScript Development](https://forums.aws.amazon.com/forum.jspa?forumID=148)
+ [\.NET Development](https://forums.aws.amazon.com/forum.jspa?forumID=61)

\(When you enter these forums, AWS might require you to sign in\.\) 

You can also [contact us](https://aws.amazon.com/contact-us/) directly\. 

### Report a Bug with the AWS Toolkit or Make a Feature Request<a name="welcome-issues"></a>

To report a bug with the AWS Toolkit for JetBrains or to make a feature request, go to the [Issues](https://github.com/aws/aws-toolkit-jetbrains/issues) tab in the [aws/aws\-toolkit\-jetbrains](https://github.com/aws/aws-toolkit-jetbrains) repository on the GitHub website\. Choose **New issue**, and then follow the on\-screen instructions to finish making your bug report or feature request\. \(When you enter this website, GitHub might require you to sign in\.\)

### Contribute to the AWS Toolkit<a name="welcome-contribute"></a>

We greatly value your contributions to the AWS Toolkit\. To begin contributing, read the [Contributing Guidelines](https://github.com/aws/aws-toolkit-jetbrains/blob/master/CONTRIBUTING.md) in the [aws/aws\-toolkit\-jetbrains](https://github.com/aws/aws-toolkit-jetbrains) repository on the GitHub website\. \(When you enter this website, GitHub might require you to sign in\.\)