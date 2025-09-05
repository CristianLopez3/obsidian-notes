
Amazon Elastic File System

Amazon EFS is a fully managed, scalable file storage service for use with AWS cloud services and on-premises resources. It operates using the _Linux Network File System (NFS) protocol_, and _automatically scales_ to petabytes as you add or remove files without disrupting applications. EFS is designed to support a wide variety of workloads and can be accessed by _multiple EC2 instances simultaneously_.

## Amazon EFS benefits

##### Multi-AZ redundancy
Amazon EFS automatically replicates data across multiple Availability Zones in a region for high availability. This built-in redundancy protects against AZ failures and provides continuous access to your file systems.

##### Shared access
Amazon EFS supports thousands of concurrent NFS connections, so multiple EC2 instances can access the same file system simultaneously. This shared access model makes EFS ideal for collaborative workloads and distributed applications.

##### Elastic storage
Amazon EFS automatically grows and shrinks as you add and remove files, with no need to provision or manage storage capacity. And since you only pay for the storage you use, it's cost-effective for varying workload demands.


### Amazon EFS storage classes

With Amazon EFS, you can create and configure file systems quickly without any minimum fee or setup cost. You pay only for the storage used and you can choose from a range of storage classes designed to fit your use case.

To learn more about the Amazon EFS storage classes, choose each of the following three tabs.


**Standard storage classes**
The _EFS Standard_ and _EFS Standard-Infrequent Access (Standard-IA)_ storage classes offer Multi-AZ resilience and the highest levels of durability and availability. They have a higher cost associated with them due to higher availability and durability.

**One zone storage classes**
The _EFS Standard_ and _EFS Standard-Infrequent Access (Standard-IA)_ storage classes offer Multi-AZ resilience and the highest levels of durability and availability. They have a higher cost associated with them due to higher availability and durability

**Archive storage classes**
The _EFS Archive_ storage class is cost-optimized for data that is accessed only a few times a year or less and that does not need the sub-millisecond latencies of EFS Standard. EFS Archive offers a storage price up to 50% lower compared to EFS Infrequent Access, providing a more cost-optimized experience for cold, rarely-accessed data.


### Amazon EFS data lifecycle

You can further optimize Amazon EFS storage costs by automatically moving data between storage classes based on usage patterns. You can create lifecycle policies that determine when and how files transition between different storage tiers. These automated policies help ensure your data resides in the most cost-effective storage class without manual intervention.

#### Transition to IA

This policy instructs lifecycle management when to move files into the Infrequent Access storage, which is cost-optimized for data that is accessed only a few times each quarter. By default, files that are not accessed in Standard storage for 30 days are transitioned into IA.

#### Transition to Archive

This policy instructs lifecycle management when to move files into the Archive storage class, which is cost-optimized for data that is accessed only a few times each year or less. By default, files that are not accessed in Standard storage for 90 days are transitioned into Archive.

#### Transition to Standard

This policy instructs lifecycle management whether to transition files out of IA or Archive and back into Standard storage when the files are accessed in the IA or Archive storage. By default, files are not moved back to Standard storage, and they remain in the IA or Archive storage class when they are accessed.