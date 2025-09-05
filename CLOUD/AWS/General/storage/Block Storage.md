
* Data divided into pieces called blocks.
* direct data access without file system layers.
* Best for applications / databases needing fast, frequent updates.


Block storage provides persistent, low-latency block-level storage volumes that attach to EC2 instances like physical hard drives. Block storage volumes can be encrypted, backed up via snapshots, and modified while in use without disrupting the instance. AWS offers two primary block storage services:

- _Amazon EC2 instance store_  
    An unmanaged non-persistent, high-performance block storage directly attached to EC2 instances for temporary data.
    
- _Amazon Elastic Block Store (EBS)_  
    A managed service that provides persistent block storage volumes for EC2 instances, offering various types for different workloads