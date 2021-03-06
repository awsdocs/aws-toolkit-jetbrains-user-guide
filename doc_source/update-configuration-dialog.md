# Update Configuration dialog box<a name="update-configuration-dialog"></a>

The **Update Configuration** dialog box in the AWS Toolkit for JetBrains is displayed whenever you [update the configuration for an AWS Lambda function](key-tasks.md#key-tasks-lambda-update)\. The information that you provide differs slightly depending on whether the project's Lambda function is of package type `Zip` or `Image`\.

The **Update Configuration** dialog box for the `Zip` package type:

![\[The Update Configuration dialog box for Zip applications.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **Update Configuration** dialog box for the `Image` package type:

![\[The Update Configuration dialog box for Image applications.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **Update Configuration** dialog box contains the following items:

**Name**  
\(Required\) The function's name\. Can contain only the uppercase letters `A` through `Z`, the lowercase letters `a` through `z`, the numbers `0` through `9`, hyphens \(`-`\), and underscores \(`_`\)\. The name must be less than 64 characters in length\.

**Description**  
\(Optional\) Any meaningful description about the function\.

**Package Type**  
\(Required\) The Lambda function's package type, which can be either `Zip` or `Image`\.

**Handler**  
\(Required for `Zip` packages only\) The ID of the corresponding Lambda function handler for [Java](https://docs.aws.amazon.com/lambda/latest/dg/java-handler.html), [Python](https://docs.aws.amazon.com/lambda/latest/dg/python-handler.html), [Node\.js](https://docs.aws.amazon.com/lambda/latest/dg/nodejs-handler.html), or [C\#](https://docs.aws.amazon.com/lambda/latest/dg/csharp-handler.html)\.

**Runtime**  
\(Required for `Zip` packages only\) The ID of the [Lambda runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) to use\.

**Timeout \(seconds\)**  
\(Required\) The amount of time that Lambda allows a function to run before stopping it\. Specify an amount up to 900 seconds \(15 minutes\)\.

**Memory \(MB\)**  
\(Required\) The amount of memory available to the function as it runs\. Specify an amount [between 128 MB and 3,008 MB](https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html) in 64\-MB increments\.

**Environment Variables**  
\(Optional\) Any [environment variables](https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html) for the Lambda function to use, specified as key\-value pairs\. To add, change, or delete environment variables, choose the folder icon, and then follow the on\-screen instructions\.

**IAM Role**  
\(Required\) Choose an available [Lambda execution role](https://docs.aws.amazon.com/lambda/latest/dg/lambda-intro-execution-role.html) in the connected AWS account for Lambda to use for the function\. To create an execution role in the account and have Lambda use that role instead, choose **Create**, and then follow the on\-screen instructions\.

**Enable AWS X\-Ray**  
\(Optional\) If selected, [Lambda enables AWS X\-Ray](https://docs.aws.amazon.com/lambda/latest/dg/services-xray.html) to detect, analyze, and optimize performance issues with the function\. X\-Ray collects metadata from Lambda and any upstream or downstream services that make up your function\. X\-Ray uses this metadata to generate a detailed service graph that shows performance bottlenecks, latency spikes, and other issues that impact function performance\.