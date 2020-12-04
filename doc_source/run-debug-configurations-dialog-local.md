# Run/Debug Configurations dialog box \(local function settings\)<a name="run-debug-configurations-dialog-local"></a>

This dialog box is displayed whenever you update settings for the *local* version of an AWS Lambda function\.

**Note**  
To update settings for the *remote* version of that same function \(the function's source code is in Lambda in your AWS account\), see [Run/Debug Configurations dialog box \(remote function settings\)](run-debug-configurations-dialog-remote.md) instead\.

This dialog box contains three tabs: **Configuration**, **SAM CLI**, and **AWS Connection**\.

![\[The Configuration tab of the Run/Debug Configurations dialog box for local function settings.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **Configuration** tab of the **Run/Debug Configurations** dialog box for local function settings contains the following items:

**Name**  
\(Required\) The name of this configuration\.

**Allow parallel run / Allow running in parallel **  
\(Optional\) If selected, allows IntelliJ IDEA, PyCharm, WebStorm, or JetBrains Rider to launch as many instances of the configuration to run in parallel as needed\.1

**From handler / From template**  
\(Required\) Depending on which option you choose, you must configure additional settings\.

**Runtime**  
\(Required\) The ID of the [Lambda runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) to use\.

**Handler**  
\(Required for the **From handler** option\) The identifier of the corresponding function handler for [Java](https://docs.aws.amazon.com/lambda/latest/dg/java-handler.html), [Python](https://docs.aws.amazon.com/lambda/latest/dg/python-handler.html), [Node\.js](https://docs.aws.amazon.com/lambda/latest/dg/nodejs-handler.html), or [C\#](https://docs.aws.amazon.com/lambda/latest/dg/csharp-handler.html)\.

**Timeout \(seconds\)**  
\(Required for the **From handler** option\) The amount of time that Lambda allows a function to run before stopping it\. Specify an amount up to 900 seconds \(15 minutes\)\.

**Memory \(MB\)**  
\(Required for the **From handler** option\) The amount of memory available to the function as it runs\. Specify an amount [between 128 MB and 3,008 MB](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html) in 64\-MB increments\.

**Environment Variables**  
\(Optional for the **From handler** option\) Any [environment variables](https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html) for the Lambda function to use, specified as key\-value pairs\. To add, change, or delete environment variables, choose the folder icon, and then follow the on\-screen instructions\.

**Template**  
\(Required for the **From template** option\) The location and file name of the AWS Serverless Application Model \(AWS SAM\) template \(for example, `template.yaml`\) to use for this configuration, and the resource in that template to associate with this configuration\.

**File**  
\(Required\) The location and file name of the event data to pass to the function, in JSON format\. For event data examples, see [Invoke the Lambda function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating sample event payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.

**Text**  
\(Required\) The event data to pass to the function, in JSON format\. For event data examples, see [Invoke the Lambda function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating sample event payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.  
Either **File** or **Text** is required, but not both\.

**Before launch: window**  
\(Optional\) Lists any tasks that must be performed before starting this configuration\.2

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

![\[The SAM CLI tab of the Run/Debug Configurations dialog box for local function settings.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **SAM CLI** tab of the **Run/Debug Configurations** dialog box for local function settings contains the following items:

**Name**  
\(Required\) The name of this configuration\.

**Allow parallel run / Allow running in parallel**  
\(Optional\) If selected, allows IntelliJ IDEA, PyCharm, WebStorm, or JetBrains Rider to launch as many instances of the configuration to run in parallel as needed\.1

**Build function inside a container**  
\(Optional\) If selected, the AWS SAM CLI builds any of the serverless application's functions inside of a Lambda\-like Docker container locally before deployment\. This is useful if the function depends on packages that have natively compiled dependencies or programs\. For more information, see [Building applications](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-build.html) in the *AWS Serverless Application Model Developer Guide*\.

**Skip checking for newer container images**  
\(Optional\) If selected, the AWS SAM CLI skips pulling down the latest Docker image for the [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) that is specified on the **Configuration** tab\.

**Docker Network**  
\(Optional\) The name or ID of an existing Docker network for Lambda Docker containers to connect to, with the default bridge network\. If not specified, the Lambda containers connect only to the default bridge Docker network\.

**Before launch: window**  
\(Optional\) Lists any tasks that must be performed before starting this configuration\.2

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

![\[The AWS Connection tab of the Run/Debug Configurations dialog box for local function settings.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **AWS Connection** tab of the **Run/Debug Configurations** dialog box for local function settings contains the following items:

**Credentials**  
\(Required\) The name of the existing [AWS account connection](key-tasks.md#key-tasks-connections) to use\.

**Region**  
\(Required\) The name of the [AWS Region](key-tasks.md#key-tasks-switch-region) to use for the connected account\.

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