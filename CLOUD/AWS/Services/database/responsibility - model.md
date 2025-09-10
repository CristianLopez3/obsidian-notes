
The AWS shared responsibility model groups services into three categories based on the ownership of administrative tasks. These categories are fully managed, managed, and unmanaged. The AWS services that you will be exploring in this module are primarily fully managed, with a few managed services, and no unmanaged services.

To learn more about how these categories relate to database services, expand the following three categories.

#### Fully managed services
For fully managed services, AWS handles nearly all operational tasks like provisioning, scaling, patching, backups, performance optimization, and security patches. AWS also provides built-in monitoring and metrics. Fully managed AWS database services only require customers to be responsible for designing data structures and managing access controls.

![[Pasted image 20250909211755.png]]


#### Managed services
With managed database services, AWS handles routine tasks like backups, patching, and hardware provisioning while customers are responsible for database configuration, query optimization, and performance tuning decisions.

![[Pasted image 20250909211815.png]]

#### Unmanaged services
With unmanaged databases, customers are responsible for installation, configuration, patching, maintenance tasks, database security, backups, high availability setup, and performance optimization. An example of an unmanaged database in AWS would be a database management system like MySQL installed directly on an Amazon Elastic Compute Cloud (Amazon EC2) instance.


![[Pasted image 20250909211848.png]]