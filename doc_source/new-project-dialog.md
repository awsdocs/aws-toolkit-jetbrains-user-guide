# New Project Dialog<a name="new-project-dialog"></a>

The **New Project** dialog in the AWS Toolkit for JetBrains displays whenever you [create an AWS serverless application](key-tasks.md#key-tasks-sam-create)\.

**Topics**
+ [New Project Dialog \(IntelliJ IDEA\)](#new-project-dialog-intellij)
+ [New Project Dialog \(PyCharm\)](#new-project-dialog-pycharm)

## New Project Dialog \(IntelliJ IDEA\)<a name="new-project-dialog-intellij"></a>

![\[The New Project dialog for IntelliJ IDEA\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **New Project** dialog contains the following items\.

**Project name**  
*Required*\. The name of the project\.

**Project location**  
*Required*\. The location where IntelliJ IDEA will create the project\.

**Runtime**  
*Required*\. The identifier of the [runtime](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html) for Lambda to use\.

**SAM Template**  
*Required*\. The name of the AWS Serverless Application Model \(AWS SAM\) template to use\.

**Project SDK**  
*Required*\. The Java SDK \(JDK\) to use\. For more information, see [Configure the JDK when creating a project](https://www.jetbrains.com/help/idea/creating-and-managing-projects.html#configure-jdk) on the IntelliJ IDEA Help website\.

**Module name**  
*Required*\. The name of the module to create\. For more information, see [Modules](https://www.jetbrains.com/help/idea/creating-and-managing-modules.html#Creating_and_Managing_Modules.xml) on the IntelliJ IDEA Help website\.

**Content root**  
*Required*\. The location where IntelliJ IDEA will create the project's content root\. For more information, see [Content roots](https://www.jetbrains.com/help/idea/content-roots.html#Content_roots.xml) on the IntelliJ IDEA Help website\.

**Module file location**  
*Required*\. The location where IntelliJ IDEA will create the module\. For more information, see [Modules](https://www.jetbrains.com/help/idea/creating-and-managing-modules.html#Creating_and_Managing_Modules.xml) on the IntelliJ IDEA Help website\.

**Project format**  
*Required*\. The format of the project that IntelliJ IDEA will create\. For more information, see [Project formats](https://www.jetbrains.com/help/idea/creating-and-managing-projects.html#project-formats) on the IntelliJ IDEA Help website\.

## New Project Dialog \(PyCharm\)<a name="new-project-dialog-pycharm"></a>

![\[The New Project dialog for PyCharm\]](http://docs.aws.amazon.com/toolkit-for-jetbrains/latest/userguide/)

The **New Project** dialog contains the following items\.

**Location**  
*Required*\. The location where PyCharm will create the project\. For more information, see [Project](https://www.jetbrains.com/help/pycharm/project.html) on the PyCharm Help website\.

**SAM Template**  
*Required*\. The name of the AWS Serverless Application Model \(AWS SAM\) template to use\.

**New environment using / Existing interpreter**  
Either **New environment using** or **Existing interpreter** is *required* \(but not both\)\. Information about the interpreter that PyCharm will use when creating the project\. For more information, see [Configure a Python interpreter](https://www.jetbrains.com/help/pycharm/configuring-python-interpreter.html#Configuring__language__Interpreter.xml) on the PyCharm Help website\.