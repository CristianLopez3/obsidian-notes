Aurora is a managed relational database designed to help reduce unnecessary I/O operations. It's compatible with MySQL and PostgreSQL, provides high performance and availability, and automatically scales alongside your workloads. Aurora replicates data across multiple Availability Zones for enhanced durability and fault tolerance, and features automated backups, encryption at rest, and continuous monitoring.

### Use cases

Some examples of practical use cases for Aurora are gaming applications, media and content management, and real-time analytics.

## Benefits

#### High performance and availability
Aurora delivers up to five times the throughput of standard MySQL and three times the throughput of PostgreSQL. It uses a distributed storage system across multiple nodes to provide high performance and availability.

#### Automated storage and backup management
Aurora automatically grows storage from 10 GB to 128 TB based on your actual data usage, which eliminates guesswork in capacity planning. It also continuously backs up your database to Amazon Simple Storage Service (Amazon S3) to provide point-in-time recovery.

#### Advanced replication and fault tolerance
Aurora replicates data across three Availability Zones with six copies of data, and provides 99.99% availability. It automatically detects database failures and redirects traffic to healthy replicas without data loss.