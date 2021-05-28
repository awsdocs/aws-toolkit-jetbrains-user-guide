# Run/Debug Configurations dialog box \(remote function settings\)<a name="run-debug-configurations-dialog-remote"></a>

This dialog box displays whenever you update settings for the *remote* version of an AWS Lambda function \(the function's source code is in Lambda in your AWS account\)\.

**Note**  
To update settings for the *local* version of that same function, see [Run/Debug Configurations dialog box \(local function settings\)](run-debug-configurations-dialog-local.md) instead\.  
Although the name of the dialog box is **Run/Debug Configurations**, you cannot use the AWS Toolkit for JetBrains to debug the remote version of a Lambda function\. You can only run the function\.

![\[The Run/Debug Configurations dialog box for remote function settings.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **Run/Debug Configurations** dialog box for remote function settings contains the following items:

**Name**  
\(Required\) The name of this configuration\.

**Share / Share through VCS**  
\(Optional\) If selected, makes this configuration available to other team members\.1

**Allow parallel run / Allow running in parallel **  
\(Optional\) If selected, allows IntelliJ IDEA, PyCharm, WebStorm, or JetBrains Rider to launch as many instances of the configuration to run in parallel as needed\.1

**Credentials**  
\(Required\) The name of the existing [AWS account connection](key-tasks.md#key-tasks-connections) to use\.

**Region**  
\(Required\) The name of the [AWS Region](key-tasks.md#key-tasks-switch-region) to use for the connected account\.

**Function**  
\(Required\) The name of the Lambda function to use\.

**File**  
\(Required\) The location and file name of the event data to pass to the function, in JSON format\. For event data examples, see [Invoke the Lambda function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating sample event payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.

**Text**  
\(Required\) The event data to pass to the function, in JSON format\. For event data examples, see [Invoke the Lambda function](https://docs.aws.amazon.com/lambda/latest/dg/getting-started-create-function.html#get-started-invoke-manually) in the *AWS Lambda Developer Guide* and [Generating sample event payloads](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-generate-event.html) in the *AWS Serverless Application Model Developer Guide*\.

**Note**  
Either **File** or **Text** is required, but not both\.

**Before launch: Activate tool window**  
\(Optional\) Lists any tasks that must be performed before starting this configuration\.2

**Show this page**  
\(Optional\) If selected, displays these configuration settings prior to starting this configuration\.2

**Activate tool window**  
\(Optional\) If selected, opens the **Run** or the **Debug** tool window when you start this configuration\.2

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