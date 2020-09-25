# Connecting to an Amazon Redshift cluster<a name="redshift-connection"></a>

With **AWS Explorer**, you can select an Amazon Redshift cluster, choose an authentication method, and then configure the connection settings\. After you've successfully tested the connection, you can start interacting with the data source using JetBrains DataGrip\. 

**Important**  
Ensure that you've completed the [prerequisites](redshift-access-prerequisities.md) to enable users to access and interact with Amazon Redshift clusters and databases\.

Select a tab for instructions on connecting to a cluster using your preferred authentication method\.

------
#### [ Connect with IAM credentials ]

1. [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open\.

1. Click the **Amazon Redshift** node to expand the list of available clusters\.

1. Right\-click a cluster and choose **Connect with IAM credentials**\.
**Note**  
You can also choose **Copy Arn** to add the cluster's Amazon Resource Name \(ARN\) to your clipboard\.

1. In the **Data Sources and Drivers** dialog box, do the following to ensure a database connection can be opened:
   + In the **Imported Data Sources** pane, confirm that the correct data source is selected\.
   + If a message indicates that you need to **Download missing driver files**, choose **Go to Driver** \(the wrench icon\) to download the required files\.

1. On the **General** tab of the **Settings** pane, confirm that the following fields display the correct values: 
   + **Host/Port** – The endpoint and port used for connections to the cluster\. For Amazon Redshift clusters hosted in the AWS Cloud, endpoints always end with `redshift.amazon.com`\.
   + **Authentication** – **AWS IAM** \(authentication using IAM credentials\)\. 
   + **User** – The name of your database user account\.
   + **Credentials** – The credentials used to access your AWS account\. 
   + **Region** – The AWS Region where the database is hosted\. 
   + **Cluster ID** – The ID of the cluster you selected in **AWS Explorer**\. 
   + **Database** – The name of the database in the cluster you'll connect to\. 
   + **URL** – The URL that the JetBrains IDE will use to connect to the cluster's database\.  
![\[Connection settings for a Amazon Redshift cluster with IAM credentials used for authentication.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
**Note**  
For a full description of the connection settings that you can configure using the **Data sources and drivers** dialog box, see the [documentation for the JetBrains IDE](https://www.jetbrains.com/help/) that you're using\. 

1. To verify the connection settings are correct, choose **Test Connection**\.

   A green check mark indicates a successful test\.

1. Choose **Apply** to apply your settings, and then choose **OK** to start working with the data source\.

   The **Database** tool window opens\. This displays the available data sources as a tree with nodes representing database elements such as schemas, tables, and keys\. 
**Important**  
To use the **Database** tool window, you must first download and install DataGrip from JetBrains\. For more information, see [https://www\.jetbrains\.com/datagrip/](https://www.jetbrains.com/datagrip/)\. 

------
#### [ Connect with Secrets Manager ]

1. [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open\.

1. Click the **Amazon Redshift** node to expand the list of available clusters\.

1. Right\-click a cluster and choose **Connect with Secrets Manager**\.
**Note**  
You can also choose **Copy Arn** to add the cluster's Amazon Resource Name \(ARN\) to your clipboard\.

1. In the **Select a Database Secret** dialog box, use the drop\-down field to pick credentials for the database, and then choose **Create**\.

1. In the **Data Sources and Drivers** dialog box, do the following to ensure a database connection can be opened:
   + In the **Imported Data Sources**, confirm that the correct the correct data source is selected\.
   + If a message appears in the dialog box to **Download missing driver files**, choose **Go to Driver** \(the wrench icon\) to download the required files\.

1. On the **General** tab of the **Settings** pane, confirm that the following fields display the correct values: 
   + **Host/Port** – The endpoint and port used for connections to the cluster\. For Amazon Redshift clusters hosted in the AWS Cloud, endpoints always end with `redshift.amazon.com`\.
   + **Authentication** – **SecretsManager Auth** \(authentication using AWS Secrets Manager\)\. 
   + **Credentials** – The credentials used to connect to the AWS account\. 
   + **Region** – The AWS Region where the cluster is hosted\. 
   + **Secret Name/ARN** – The name and ARN of the secret containing authentication credentials\. If you want to override the connection settings in the **Host/Port** fields, select the **Use the url and port from the secret** check box\.
   + **Database** – The name of the database in the cluster you'll connect to\. 
   + **URL** – The URL that the JetBrains IDE will use to connect to the database\.
**Note**  
If you're using AWS Secrets Manager for authentication, there are no fields for specifying a user name and password for the cluster\. This information is contained in the encrypted secret data portion of a secret\.  
![\[Connection settings for a Amazon Redshift cluster with Secrets Manager used for authentication.\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)
**Note**  
For a full description of the connection settings that you can configure using the **Data sources and drivers** dialog box, see the [documentation for the JetBrains IDE](https://www.jetbrains.com/help/) that you're using\. 

1. To verify the connection settings are correct, choose **Test Connection**\.

   A green check mark indicates a successful test\.

1. Choose **Apply** to apply your settings, and then choose **OK** to start working with the data source\.

   The **Database** tool window opens\. This displays the available data sources as a tree with nodes representing database elements such as schemas, tables, and keys\. 
**Important**  
To use the **Database** tool window, you must first download and install DataGrip from JetBrains\. For more information, see [https://www\.jetbrains\.com/datagrip/](https://www.jetbrains.com/datagrip/)\. 

------