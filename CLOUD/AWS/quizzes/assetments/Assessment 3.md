
A development team at an e-commerce company is working on a new website. The application runs fine on their local machines, but when they attempt to deploy it to a staging environment, it does not work as expected. The team wants to make sure that the application runs consistently across all development, testing, and production environments going forward.

Which solution should the team use to make sure that the application runs the same across all environments?

* [ ] Set up separate environments for each operating system
* [x] Package the application in a container that includes all dependencies.
* [ ] Use different versions of the applications for different environments.
* [ ] Use Amazon EC2 to manually recreate the development environment.

>[!NOTE]
>Containers bundle the application, runtime, and dependencies together, providing consistency across all environments from development to production.\

A development team at a travel company has stored their hotel booking system’s container image in Amazon Elastic Container Registry (Amazon ECR) and is ready to deploy it. They need a service that can automatically start and stop containers based on traffic, scale up or down with demand, and monitor the health of the system.

Which service does the team need next?

* [ ] AWS Lambda
* [x] An orchestration service like Amazon Elastic Container Service (Amazon ECS) or Amazon Elastic Kubernetes Service (Amazon EKS)
* [ ] A virtual machine to run the container manually
* [ ] Amazon EC2 with auto scaling

>[!NOTE]
>Amazon ECS or Amazon EKS can automatically scale containers, handle health checks, and manage their lifecycle based on traffic demand, which fits the team’s requirements.


A pharmaceutical research company needs to run thousands of simulations to analyze protein folding. These compute-heavy tasks are run in parallel and do not require real-time interaction. The company wants the jobs to be automatically scheduled and scaled based on computing demand.

Which AWS service BEST fits this workload?

* [ ] Amazon Lightsail
* [x] AWS Batch
* [ ] AWS Lambda
* [ ] AWS Elastic Beanstalk

>[!NOTE]
>AWS Batch is designed for large-scale batch workloads and can automatically manage and scale compute resources for job queues.



Which scenario is the BEST fit for using AWS Lambda?

* [ ] Running a large, high-performance computing workload that takes several hours to complete
* [ ] Running a relational database that needs complex queries and frequent connections
* [ ] Hosting a high-traffic web server that requires full control over the operating system (OS)
* [x] Automatically processing images as users upload them to an Amazon S3 bucket

>[!NOTE]
>Lambda is perfect for this event-driven use case. It can run code in response to uploads and scale automatically based on the number of events.


A company is launching a containerized photo application and has built the container image, which needs to be stored securely. They plan to use Kubernetes for orchestration and prefer not to manage any servers.

  
Which combination of AWS services BEST fits their needs?

* [ ] Amazon Elastic Container Registry (Amazon ECR), AWS Lambda, and Amazon EC2
* [ ] Amazon S3, Amazon Elastic Container Service (Amazon ECS), and Amazon EC2
* [x] Amazon Elastic Container Registry (Amazon ECR), Amazon Elastic Kubernetes Service (Amazon EKS), and AWS Fargate
* [ ] Amazon Elastic Container Registry (Amazon ECR), Amazon Elastic Container Service (Amazon ECS), and Amazon EC2

>[!NOTE]
>Amazon ECR stores container images, Amazon EKS handles Kubernetes orchestration, and AWS Fargate runs containers without server management. This combination offers seamless orchestration with no infrastructure maintenance.

A freelance developer is building a blog for a client with minimal traffic. They want a basic, cost-effective solution that includes storage and compute in one package, without having to deal with complex configurations or scaling concerns.

Which AWS service is the BEST fit?

* [x] Amazon Lightsail
* [ ] AWS Batch
* [ ] AWS Fargate
* [ ] AWS Lambda

>[!NOTE]
>Lightsail is great for small projects like blogs and basic websites, and it offers predictable pricing and ease of use.


What is the customer responsible for managing in a serverless service like AWS Lambda?

* [ ] The physical servers and networking hardware
* [x] The application code
* [ ] The operating system, network configuration, and application stack
* [ ] Nothing—AWS manages everything

A developer is launching a new microservice and wants to focus only on writing and deploying code. They do not want to manage servers, handle scaling, or worry about infrastructure availability.

Which AWS service model is BEST for this use case?

* [ ] Hybrid cloud
* [ ] Unmanaged
* [ ] On premises
* [ ] Serverless

>[!NOTE]
>With serverless services, customers can focus solely on writing and deploying code. AWS fully manages infrastructure, scaling, and availability, so customers do not have to worry about managing servers or capacity.

