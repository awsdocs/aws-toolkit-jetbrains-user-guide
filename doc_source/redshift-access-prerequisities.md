# Prerequisites for accessing Amazon Redshift clusters<a name="redshift-access-prerequisities"></a>

Before you start can interacting with an Amazon Redshift cluster using AWS Toolkit for JetBrains, you need to complete the following tasks: 
+ [Create an Amazon Redshift cluster and set up its authentication method](#cluster-authentication)
+ [Download and install DataGrip](#datagrip-info-rs)

## Creating an Amazon Redshift cluster and configuring an authentication method<a name="cluster-authentication"></a>

 AWS Toolkit for JetBrains enables you to connect to an Amazon Redshift cluster that's already created and configured in AWS\. Each cluster contains one or more databases\. For information about creating and configuring Amazon Redshift clusters, see [Getting started with Amazon Redshift](https://docs.aws.amazon.com/redshift/latest/gsg/getting-started.html) in the *Amazon Redshift Getting Started*\.

When connecting to a cluster using AWS Toolkit for JetBrains, users can choose to authenticate using IAM credentials or AWS Secrets Manager\. The following table describes key features and information resources for both options: 


****  

| Authentication methods | How it works | More information | 
| --- | --- | --- | 
|  Connect with IAM credentials  |  With IAM database authentication, you don't need to store user credentials in the database because authentication is managed externally using AWS Identity and Access Management \(IAM\) credentials\.By default, IAM database authentication is disabled on database instances\. You can enable IAM database authentication \(or disable it again\) using the AWS Management Console, AWS CLI, or the API\.   |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/redshift-access-prerequisities.html)  | 
|  Connect with AWS Secrets Manager;  |  A database administrator can store credentials for a database as a secret in Secrets Manager\. Secrets Manager encrypts and stores the credentials within the secret as the *protected secret text*\. When an application with permissions accesses the database, Secrets Manager decrypts the protected secret text and returns it over a secured channel\. The client parses the returned credentials, connection string, and any other required information and then uses that information to access the database\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/redshift-access-prerequisities.html)  | 

## Working with Amazon RDS databases using DataGrip<a name="datagrip-info-rs"></a>

After you've connected to a database in Amazon Redshift cluster, you can start interacting with it\. Using DataGrip from JetBrains, you can carry out database tasks such as writing SQL, running queries, and importing/exporting data\. Features provided by DataGrip are also available in the database plugin for a range of JetBrains IDEs\. For information about DataGrip, see [https://www\.jetbrains\.com/datagrip/](https://www.jetbrains.com/datagrip/)\.