# Edit Configuration Dialog<a name="edit-configuration-dialog"></a>

The **Edit configuration** dialog in the AWS Toolkit for JetBrains displays whenever you [change \(update\) the configuration for an AWS Lambda function](key-tasks.md#key-tasks-lambda-update)\.

This dialog contains two tabs—**Configuration** and **SAM CLI**—as follows\.

![\[The Configuration tab of the Edit configuration dialog\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **Configuration** tab of the **Edit configuration** dialog contains the following items\.

**Name**  
*Required*\. The name of this configuration\.

**Share**  
*Optional*\. If selected, makes this configuration available to other team members\.  
For more information, for IntelliJ IDEA, see [Common options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#common) on the IntelliJ IDEA Help website\. For PyCharm, see see [Common options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#common) on the PyCharm Help website\.

**Allow parallel run**  
*Optional*\. If selected, allows IntelliJ IDEA or PyCharm to launch as many instances of the configuration to run in parallel as needed\.  
For more information, for IntelliJ IDEA, see [Common options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#common) on the IntelliJ IDEA Help website\. For PyCharm, see see [Common options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#common) on the PyCharm Help website\.

**From template**  
*Required*\. The location and file name of the AWS Serverless Application Model \(AWS SAM\) template \(for example, `template.yaml`\) to use for this configuration, as well as the resource in that template to associate with this configuration\.

**Runtime**  
*Required*\. The identifier of the [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) for Lambda to use\.

**Handler**  
*Required*\. The identifier of the corresponding [function handler for Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html) or the [function handler for Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html)\.

**Environment Variables**  
*Optional*\. Any [environment variables](https://docs.aws.amazon.com/lambda/latest/dg/env_variables.html) for the AWS Lambda function to use, specified as key/value pairs\. To add, change, or delete environment variables, choose the folder icon, and then follow the on\-screen instructions\.

**Credentials**  
*Required*\. The name of the existing [AWS account connection](key-tasks.md#key-tasks-connections) to use\.

**Region**  
*Required*\. The name of the [AWS Region](key-tasks.md#key-tasks-switch-region) to use for the connected account\.

**File**  
Either **File** or **Text** is *required* \(but not both\)\. The location and file name of the event data to pass into the function, expressed in JSON format\. For event data examples, see [Invoke the Lambda Function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating Sample Event Payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.

**Text**  
Either **File** or **Text** is *required* \(but not both\)\. The event data to pass into the function, expression in JSON format\. For event data examples, see [Invoke the Lambda Function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating Sample Event Payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.

**Before launch: Activate tool window**  
*Optional*\. Lists any tasks that must be performed before starting this configuration\.  
For more information, for IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.

**Show this page**  
*Optional*\. If selected, displays these configuration settings prior to starting this configuration\.  
For more information, for IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.

**Activate tool window**  
*Optional*\. If selected, opens the **Run** or the **Debug** tool window when you start this configuration\.   
For more information, for IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.

![\[The SAM CLI tab of the Edit configuration dialog\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **SAM CLI** tab of the **Edit configuration** dialog contains the following items\.

**Name**  
*Required*\. The name of this configuration\.

**Share**  
*Optional*\. If selected, makes this configuration available to other team members\.  
For more information, for IntelliJ IDEA, see [Common options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#common) on the IntelliJ IDEA Help website\. For PyCharm, see see [Common options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#common) on the PyCharm Help website\.

**Allow parallel run**  
*Optional*\. If selected, allows IntelliJ IDEA or PyCharm to launch as many instances of the configuration to run in parallel as needed\.  
For more information, for IntelliJ IDEA, see [Common options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#common) on the IntelliJ IDEA Help website\. For PyCharm, see see [Common options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#common) on the PyCharm Help website\.

**Build function inside a container**  
*Optional*\. If selected, the AWS SAM CLI builds any of the serverless application's functions inside of an AWS Lambda\-like Docker container locally before deployment\. This is useful if the function depends on packages that have natively compiled dependencies or programs\. For more information, see [Building Applications with Dependencies](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-build.html) in the *AWS Serverless Application Model Developer Guide*\.

**Skip checking for newer container images**  
*Optional*\. If selected, the AWS SAM CLI skips pulling down the latest Docker image for the [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) that is specified on the **Configuration** tab\.

**Docker Network**  
*Optional*\. The name or ID of an existing Docker network to Lambda Docker containers should connect to, along with the default bridge network\. If not specified, the Lambda containers will only connect to the default bridge Docker network\.

**Before launch: Activate tool window**  
*Optional*\. Lists any tasks that must be performed before starting this configuration\.  
For more information, for IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.

**Show this page**  
*Optional*\. If selected, displays these configuration settings prior to starting this configuration\.  
For more information, for IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.

**Activate tool window**  
*Optional*\. If selected, opens the **Run** or the **Debug** tool window when you start this configuration\.   
For more information, for IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.