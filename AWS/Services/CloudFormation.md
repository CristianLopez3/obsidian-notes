
CloudFormation is a service that helps you model and set up your AWS resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. With CloudFormation, you can define your infrastructure as code. You create a template that describes all the AWS resources that you want (like Amazon Elastic Compute Cloud EC2), and CloudFormation takes care of provisioning and configuring those resources for you.

### Interacting with AWS Resources

As you've learned, there are a number of ways you can operate in the AWS Cloud. To interact with resources, you must invoke AWS APIs. To interact with these APIs, you can use the AWS SDKs, the AWS Command Line Interface (AWS CLI), the AWS Management Console, or IaC tools such as CloudFormation. 

#### Programming Access

Programmatic access includes options like the  AWS CLI and AWS SDKs. These options are best suited for developer and those familiar with coding languages.

With the AWS CLI, you manage multiple AWS services directly from the command line. You can automate tasks through scripts.

AWS SDKs can help integrate AWS services into your applications by providing APIs for various programming languages.  AWS Provides documentation and sample code to help you get started with using SDKs.

* **AWS CLI**: Automate routine tasks. For example, you might write a script to provide routine backups for a service such as Amazon Elastic Block Store (Amazon EBS).
* **SDKs**: Invoke APIs for one part of application process. For example, you might use an SDK to store user data in an AWS storage service such as Amazon Simple Service (Amazon S3).

#### AWS Management Console

The AWS Management Console is a web interface that you use for managing AWS services, offering quick access to services, search functionality, and simplified workflows. The console is great option for those new to the cloud users with minimal or no development experience.

Use cases for using the console include the following:
* **Billing and cost optimization** dashboard and visualizations.
* **Services focused on graphical representations**, like Amazon QuickSight and Amazon Neptune.


#### Infrastructure as Code

With IaC tools such as CloudFormation, you can automate resource management across your organization with AWS service integrations offering efficient and repeatable resource creation and management.

Use cases for CloudFormation include the following:

* Managing infrastructure with DevOps such as continuous integration and delivery (CI/CD) pipelines
* Scaling resources such as Amazon EC2 instances to multi-Region applications in a consistent, repeatable way.