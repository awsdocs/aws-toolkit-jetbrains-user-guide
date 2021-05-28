# Creating App Runner services<a name="creating-service-apprunner"></a>

You can create an App Runner service in AWS Toolkit for JetBrains by using the **Create App Runner Service** dialog box\. Its interface allows you to select a source repository and configure the service instance in which your application runs\. 

Before creating an App Runner service, you should ensure that you've completed the [prerequisites](using-apprunner.md#apprunner-prereqs) related to IAM permissions and the source repository to be deployed\.<a name="create-service"></a>

# To create an App Runner service<a name="create-service"></a>

1. [Open AWS Explorer](key-tasks.md#key-tasks-open-explorer), if it isn't already open\.

1. Right\-click the **App Runner** node and choose **Create Service**\.

   The **Create App Runner Service** dialog box is displayed\.

1. Enter your unique **Service name**\.

1. Choose your source type \(**ECR**, **ECR public** or **Source code repository**\) and configure the relevant settings :

------
#### [ ECR/ECR public ]

   If you're using a private registry, choose the **Deployment type**:
   + **Manual**: Use manual deployment when you want to explicitly initiate each deployment to your service\. 
   + **Automatic**: Use automatic deployment when you want continuous integration and deployment \(CICD\) behavior for your service\. Whenever you push a new image version to your image repository, or a new commit to your code repository, App Runner automatically deploys it to your service without further action required from you\.

   For **Container image URI**, enter the URI of the image repository that you copied from your Amazon ECR private registry or Amazon ECR Public Gallery\.

   For **Start Command**, enter the command to start the service process\.

   For **Port**, enter the IP port used by the service\.

   If you're using an Amazon ECR private registry, select the required **ECR access role** and choose **Create**\.
   + The **Create IAM Role** dialog box displays the **Name**, **Managed Policies**, and **Trust Relationships** for the IAM role\. Choose **Create**\.

------
#### [ Source code repository ]

   Choose the **Deployment type**:
   + **Manual**: Use manual deployment when you want to explicitly initiate each deployment to your service\. 
   + **Automatic**: Use automatic deployment when you want continuous integration and deployment \(CICD\) behavior for your service\. Whenever you push a new image version to your image repository, or a new commit to your code repository, App Runner automatically deploys it to your service without further action required from you\.

   For **Connections**, select a connection that's available from the list on **GitHub connections** page\.

   For **Repository URL**, enter the link to remote repository hosted on GitHub\.

   For **Branch**, indicate which Git branch of your source code is to be deployed\.

   For **Configuration**, specify how you want to specify your runtime configuration:
   + **Configure all settings here**: Choose this option if you want to specify the following settings for your application's runtime environment: 
     + **Runtime**: Choose **Python 3** or **Nodejs 12**\.
     + **Port**: Enter the IP port used by the service\.
     + **Build command**: Enter the command to build your application in the service instance's runtime environment\.
     + **Start command**: Enter the command to start your application in the service instance's runtime environment\.
   + **Provide a configuration file settings here**: Choose this option to use the settings defined by the `apprunner.yaml` configuration file that's in the root directory of your application’s repository\.

------

1. Specify values to define the runtime configuration of the App Runner service instance: 
   + **CPU**: The number of CPU units reserved for each instance of your App Runner service \(Default: `1 vCPU`\)\.
   + **Memory:** The amount of memory reserved for each instance of your App Runner service \(Default: `2 GB`\)
   + **Environmental variables**: Optional environment variables that allow you to customize behavior in your service instance\. You create environmental variables by defining a key and a value\.

1. Choose **Create**

   When the service is being created, its status changes from **Operation in progress** to **Running**\.

1. After your service starts running, right\-click the service and choose **Copy Service URL**\.

1. To access your deployed application, paste the copied URL into the address bar of your web browser\.