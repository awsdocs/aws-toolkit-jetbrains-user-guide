# Working with CloudWatch Logs Insights by using the AWS Toolkit for JetBrains<a name="cloudwatch-log-insights"></a>

You can use the AWS Toolkit for JetBrains to work with CloudWatch Logs Insights\. CloudWatch Logs Insights enables you to interactively search and analyze your log data in Amazon CloudWatch Logs\. For more information, see [Analyzing Log Data with CloudWatch Logs Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html) in the *Amazon CloudWatch Logs User Guide*\.

## IAM permissions for CloudWatch Logs Insights<a name="iam-permissions-for-cwlog-insights"></a>

 You need the following permissions to run and view CloudWatch Logs Insights query results: 

```
{
  "Version": "2012-10-17",
  "Statement" : [
    {
      "Effect" : "Allow",
      "Action" : [
        "logs:StartQuery",
        "logs:GetQueryResults",
        "logs:GetLogRecord",
        "logs:describeLogGroups",
        "logs:describeLogStreams"
      ],
      "Resource" : "*"
    }
  ]
}
```

The following permission is not required but will allow the AWS Toolkit for JetBrains to automatically stop any currently running queries when you close the associated results pane or IDE\. 

```
{
  "Version": "2012-10-17",
  "Statement" : [
    {
      "Effect" : "Allow",
      "Action" : [
        "logs:StopQuery"
      ],
      "Resource" : "*"
    }
  ]
}
```

## Working with CloudWatch Logs Insights<a name="working-with-cwlog-insights"></a>

**To open the CloudWatch Logs Insights query editor**

1. [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer)\.

1.  Double\-click the **CloudWatch Logs** node to expand the list of log groups\. 

1.  Right\-click on the log group you want to open, and then choose **Open Query Editor**\. 

**To start a CloudWatch Logs Insights query**

1. In the **Query Log Groups** window, change the query parameters as desired\.

   You can choose a time range by date or relative time\.

   The **Query Log Groups** field accepts the CloudWatch Logs Insights Query Syntax\. For more information, see [CloudWatch Logs Insights Query Syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_QuerySyntax.html) in the *Amazon CloudWatch Logs User Guide*\.

1.  Choose **Execute** to begin the query\. 

**To save a CloudWatch Logs Insights query**

1.  Type a query name\. 

1.  Choose **Save Query**\. 

    The selected log groups and query are saved to your AWS account\. Time ranges are not saved\. 

   You can retrieve and reuse saved queries from the CloudWatch Logs Insights AWS Management Console page\.

**To retrieve a saved CloudWatch Logs Insights query**

1.  In the **Query Log Groups** window, choose **Retrieve Saved Queries**\. 

1.  Choose the desired query and choose **OK**\. 

   The selected log groups and query replace anything in the existing dialog\.

**To navigate through query results**
+  In the CloudWatch Logs Insights **Query Results** window, in the top right corner, choose **Open Query Editor**\. 

**To view an individual log record**
+  In the query results pane, double\-click a row to open a new tab with details about that log record\. 

   You can also navigate to the log record's associated log stream by choosing **View Log Stream** in the top right corner\. 