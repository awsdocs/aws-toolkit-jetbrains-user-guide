# Run/Debug Configurations dialog box \(local function settings\)<a name="run-debug-configurations-dialog-local"></a>

This dialog box is displayed whenever you change \(update\) settings for the *local* version of an AWS Lambda function \(the function's source code is on the local computer\)\.

**Note**  
To change \(update\) settings for the *remote* version of that same function \(the function's source code is within the Lambda service for the account\), see [Run/Debug Configurations dialog box \(remote function settings\)](run-debug-configurations-dialog-remote.md) instead\.

This dialog box contains three tabs: **Configuration**, **SAM CLI**, and **AWS Connection**\.

![\[Configuration tab of the Run/Debug Configurations dialog box for local function settings\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **Configuration** tab of the **Run/Debug Configurations** dialog box for local function settings contains the following items\.

**Name**  
*Required*\. The name of this configuration\.

**Allow parallel run / Allow running in parallel **  
*Optional*\. If selected, allows IntelliJ IDEA, PyCharm, WebStorm, or JetBrains Rider to launch as many instances of the configuration to run in parallel as needed\. 1

**From handler / From template**  
*Required*\. Radio button selection\. Depending on which option is selected, you must enter additional settings\.

**Runtime**  
*Required*\. The identifier of the [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) for Lambda to use\.

**Handler**  
*Required if 'From handler' radio button is selected*\. The identifier of the corresponding function handler for [Java](https://docs.aws.amazon.com/lambda/latest/dg/java-programming-model-handler-types.html), [Python](https://docs.aws.amazon.com/lambda/latest/dg/python-programming-model-handler-types.html), [Node\.js](https://docs.aws.amazon.com/lambda/latest/dg/nodejs-prog-model-handler.html), or [Node\.js](https://docs.aws.amazon.com/lambda/latest/dg/nodejs-prog-model-handler.html)\.

**Timeout \(seconds\)**  
*Required if 'From handler' radio button is selected*\. The amount of time that Lambda allows a function to run before stopping it\. Specify an amount of up to 900 seconds \(15 minutes\)\.

**Memory \(MB\)**  
*Required if 'From handler' radio button is selected*\. The amount of memory available to the function during its execution\. Specify an amount [between 128 MB and 3,008 MB](https://docs.aws.amazon.com/lambda/latest/dg/limits.html) in 64\-MB increments\.

**Environment Variables**  
*Optional if 'From handler' radio button is selected*\. Any [environment variables](https://docs.aws.amazon.com/lambda/latest/dg/env_variables.html) for the AWS Lambda function to use, specified as key\-value pairs\. To add, change, or delete environment variables, choose the folder icon, and then follow the on\-screen instructions\.

**Template**  
*Required if 'From template' radio button is selected*\. The location and file name of the AWS Serverless Application Model \(AWS SAM\) template \(for example, `template.yaml`\) to use for this configuration, and the resource in that template to associate with this configuration\.

**File**  
Either **File** or **Text** is *required* \(but not both\)\. The location and file name of the event data to pass into the function, expressed in JSON format\. For event data examples, see [Invoke the Lambda Function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating Sample Event Payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.

**Text**  
Either **File** or **Text** is *required* \(but not both\)\. The event data to pass into the function, expression in JSON format\. For event data examples, see [Invoke the Lambda Function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating Sample Event Payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.

**Before launch: window**  
*Optional*\. Lists any tasks that must be performed before starting this configuration\. 2

***Notes***  
1 For more information, see the following:  
+ For IntelliJ IDEA, see [Common options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#common) on the IntelliJ IDEA Help website\. 
+ For PyCharm, see [Common options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#common) on the PyCharm Help website\.
+ For WebStorm, see [Common options](https://www.jetbrains.com/help/webstorm/run-debug-configuration-node-js.html#common) on the WebStorm Help website\.
+ For JetBrains Rider, see [Common options](https://www.jetbrains.com/help/rider/Run_Debug_Configurations_dialog.html#common) on the JetBrains Rider Help website\.
2 For more information, see the following:  
+ For IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. 
+ For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.
+ For WebStorm, see [Before Launch options](https://www.jetbrains.com/help/webstorm/run-debug-configuration-node-js.html#before-launch-options) on the WebStorm; Help website\.
+ For JetBrains Rider, see [Before Launch options](https://www.jetbrains.com/help/rider/Run_Debug_Configurations_dialog.html#before-launch-options) on the JetBrains Rider Help website\.

![\[SAM CLI tab of the Run/Debug Configurations dialog box for local function settings\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **SAM CLI** tab of the **Run/Debug Configurations** dialog box for local function settings contains the following items\.

**Name**  
*Required*\. The name of this configuration\.

**Allow parallel run / Allow running in parallel **  
*Optional*\. If selected, allows IntelliJ IDEA, PyCharm, WebStorm, or JetBrains Rider to launch as many instances of the configuration to run in parallel as needed\. 1

**Build function inside a container**  
*Optional*\. If selected, the AWS SAM CLI builds any of the serverless application's functions inside of an AWS Lambda\-like Docker container locally before deployment\. This is useful if the function depends on packages that have natively compiled dependencies or programs\. For more information, see [Building Applications with Dependencies](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-build.html) in the *AWS Serverless Application Model Developer Guide*\.

**Skip checking for newer container images**  
*Optional*\. If selected, the AWS SAM CLI skips pulling down the latest Docker image for the [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) that is specified on the **Configuration** tab\.

**Docker Network**  
*Optional*\. The name or ID of an existing Docker network that Lambda Docker containers should connect to, with the default bridge network\. If not specified, the Lambda containers connect only to the default bridge Docker network\.

**Before launch: window**  
*Optional*\. Lists any tasks that must be performed before starting this configuration\. 2

***Notes***  
1 For more information, see the following:  
+ For IntelliJ IDEA, see [Common options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#common) on the IntelliJ IDEA Help website\. 
+ For PyCharm, see [Common options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#common) on the PyCharm Help website\.
+ For WebStorm, see [Common options](https://www.jetbrains.com/help/webstorm/run-debug-configuration-node-js.html#common) on the WebStorm Help website\.
+ For JetBrains Rider, see [Common options](https://www.jetbrains.com/help/rider/Run_Debug_Configurations_dialog.html#common) on the JetBrains Rider Help website\.
2 For more information, see the following:  
+ For IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. 
+ For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.
+ For WebStorm, see [Before Launch options](https://www.jetbrains.com/help/webstorm/run-debug-configuration-node-js.html#before-launch-options) on the WebStorm; Help website\.
+ For JetBrains Rider, see [Before Launch options](https://www.jetbrains.com/help/rider/Run_Debug_Configurations_dialog.html#before-launch-options) on the JetBrains Rider Help website\.

![\[The AWS Connection tab of the Run/Debug Configurations dialog box for local function settings\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **AWS Connection** tab of the **Run/Debug Configurations** dialog box for local function settings contains the following items\.

**Credentials**  
*Required*\. The name of the existing [AWS account connection](key-tasks.md#key-tasks-connections) to use\.

**Region**  
*Required*\. The name of the [AWS Region](key-tasks.md#key-tasks-switch-region) to use for the connected account\.

***Notes***  
1 For more information, see the following:  
+ For IntelliJ IDEA, see [Common options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#common) on the IntelliJ IDEA Help website\. 
+ For PyCharm, see [Common options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#common) on the PyCharm Help website\.
+ For WebStorm, see [Common options](https://www.jetbrains.com/help/webstorm/run-debug-configuration-node-js.html#common) on the WebStorm Help website\.
+ For JetBrains Rider, see [Common options](https://www.jetbrains.com/help/rider/Run_Debug_Configurations_dialog.html#common) on the JetBrains Rider Help website\.
2 For more information, see the following:  
+ For IntelliJ IDEA, see [Before Launch options](https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html#before-launch-options) on the IntelliJ IDEA Help website\. 
+ For PyCharm, see [Before Launch options](https://www.jetbrains.com/help/pycharm/run-debug-configurations-dialog.html#before-launch-options) on the PyCharm Help website\.
+ For WebStorm, see [Before Launch options](https://www.jetbrains.com/help/webstorm/run-debug-configuration-node-js.html#before-launch-options) on the WebStorm; Help website\.
+ For JetBrains Rider, see [Before Launch options](https://www.jetbrains.com/help/rider/Run_Debug_Configurations_dialog.html#before-launch-options) on the JetBrains Rider Help website\.