
|Feature|Security Groups|Network ACLs|
|---|---|---|
|**Scope**|Instance level (attached to EC2 instances)|Subnet level (associated with subnets)|
|**State**|Stateful (remembers state)|Stateless (doesn't remember state)|
|**Rule types**|Only allow type rules|Both allow and deny type rules|
|**Return traffic**|Return traffic is automatically allowed if inbound traffic is allowed|Return traffic must be implicitly allowed in both directions|
|**Uses**|Fine-grained control of traffic for individual EC2 instances|Broad control of traffic in and out of subnets|

Remember the AWS Shared Responsibility Model? When it comes to securing the subnets and resources in your VPC with network ACLs and security groups, that is your responsibility. These components make up networking traffic protection and are critical defenses in protecting your applications _IN_ the cloud.

![[Pasted image 20250811205432.png]]