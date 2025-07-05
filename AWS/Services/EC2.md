Amazon EC2 is more flexible, cost-effective, and faster than managing on-premises servers. It offers on-demand compute capacity that can be quickly launched, scaled, and terminated, with costs based only on active usage.

The flexibility of Amazon EC2 allows for faster development and deployment of applications. You can launch as many or as few virtual servers as needed and configure security, networking, and storage. You can also scale resources up or down based on usage, such as handling high traffic or compute-heavy tasks.

Key takeaways: Comparing on-premises and cloud resources

When designing infrastructure for your business, selecting the right resources can significantly affect your efficiency, flexibility, and overall costs. Review the key differences between on-premises and cloud resource management.


### How amazon EC2 works?

#### Launch
Amazon EC2 is more flexible, cost-effective, and faster than managing on-premises servers. It offers on-demand compute capacity that can be quickly launched, scaled, and terminated, with costs based only on active usage.

The flexibility of Amazon EC2 allows for faster development and deployment of applications. You can launch as many or as few virtual servers as needed and configure security, networking, and storage. You can also scale resources up or down based on usage, such as handling high traffic or compute-heavy tasks.

#### Connect
You can connect to an EC2 instance in various ways. Applications can interact with services running on the instance over the network.

Users or administrators can connect using SSH for Linux instances or Remote Desktop Protocol (RDP) for Windows instances. Alternatively, AWS services like AWS Systems Manager offer a secure and simplified method for accessing instances.


#### Use the instance
After you are connected to the instance, you can begin using it to run commands, install software, add storage, organize files, and perform other tasks.

**Key takeaways: Comparing on-premises and cloud resources**

When designing infrastructure for your business, selecting the right resources can significantly affect your efficiency, flexibility, and overall costs. Review the key differences between on-premises and cloud resource management.


## Key takeaways: EC2 instance types

Whether you're running a simple web service or complex data processing tasks, Amazon EC2 provides the flexibility to select the ideal instance type for your needs.

To review EC2 instance types, choose each of the five numbered markers.

## General purpose

General purpose instances provide a balanced mix of compute, memory, and networking resources. They are ideal for diverse workloads, like web services, code repositories, and when workload performance is uncertain.

## Compute optimized

Compute optimized instances are ideal for compute-intensive tasks, such as gaming servers, high performance computing (HPC), machine learning, and scientific modeling.

## Memory optimized

Memory optimized instances are used for memory-intensive tasks like processing large datasets, data analytics, and databases. They provide fast performance for memory-heavy workloads.

## Accelerated computing

Accelerated computing instances use hardware accelerators, like graphics processing units (GPUs), to efficiently handle tasks, such as floating-point calculations, graphics processing, and machine learning.

## Storage optimized

Storage optimized instances are designed for workloads that require high performance for locally stored data, such as large databases, data warehousing, and I/O-intensive applications.

>[!NOTE]
>Instance types are named based on their _instance family_ and _instance size_. For information about these naming conventions, refer to [Amazon EC2 instance type naming conventions(opens in a new tab)](https://docs.aws.amazon.com/ec2/latest/instancetypes/instance-type-names.html).


# Launch an EC2 image

To launch an EC2 instance for a web server, configure the AMI to define the operating system and software; select the instance type to allocate CPU, memory, and storage; and set up storage options, including the type and size of the volume.

Load balancing, permissions, and instance termination behavior are not required when launching a basic Amazon EC2 web server.


**On-Demand Instances:**  
Pay only for the compute capacity you consume with no upfront payments or long-term commitments required.

**Reserved Instances:** Get a savings of up to 75 percent by committing to a 1-year or 3-year term for predictable workloads using specific instance families and AWS Regions.

**Spot Instances**: Bid on spare compute capacity at up to 90 percent off the On-Demand price, with the flexibility to be interrupted when AWS reclaims the instance.

**Savings Plans:** Save up to 72 percent across a variety of instance types and services by committing to a consistent usage level for 1 or 3 years.

**Dedicated Hosts:** Reserve an entire physical server for your exclusive use. This option offers full control and is ideal for workloads with strict security or licensing needs.

**Dedicated Instances:** Pay for instances running on hardware dedicated solely to your account. This option provides isolation from other AWS customers.


## Amazon EC2 Auto Scaling

Amazon EC2 Auto Scaling automatically adjusts the number of EC2 instances based on changes in application demand, providing better availability. It offers two approaches. _Dynamic scaling_ adjusts in real time to fluctuations in demand. _Predictive scaling_ preemptively schedules the right number of instances based on anticipated demand.


##### **Example: Amazon EC2 Auto Scaling**

With EC2 Auto Scaling, you maintain the desired amount of compute capacity for your application by dynamically adjusting the number of EC2 instances based on demand. You can create Auto Scaling groups, which are collections of EC2 instances that can scale in or out to meet your application’s needs.

An Auto Scaling group is configured with the following three key settings.

**Minimun**
The _minimum capacity_ defines the least number of EC2 instances required to keep the application running. This makes sure that the system never scales below this threshold. It's the number of EC2 instances that launch immediately after you have created the Auto Scaling group. 

In this example, the minimum capacity is four EC2 instances.'

**Desired Capacity**
The _desired capacity_ is the ideal number of instances needed to handle the current workload, which Auto Scaling aims to maintain. If you do not specify the desired number of EC2 instances in an Auto Scaling group, the desired capacity defaults to your minimum capacity.

In this example, the desired capacity is six EC2 instances.

**Maximum Capacity**
The _maximum capacity_ sets an upper limit on the number of instances that can be launched, preventing over-scaling and controlling costs. For example, you might configure the Auto Scaling group to scale out in response to increased demand.

In this example, a maximum of 12 EC2 instances can be launched. Amazon EC2 Auto Scaling will scale between the minimum and maximum number of instances.

Because Amazon EC2 Auto Scaling uses EC2 instances, you pay for only the instances you use, when you use them. This gives you a cost-effective architecture that provides the best customer experience while reducing expenses.