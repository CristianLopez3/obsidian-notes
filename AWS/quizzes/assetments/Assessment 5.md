
What is the primary function of a domain name service (DNS)?

* [ ] It filters inbound and outbound traffic to Amazon EC2 instances in a virtual private cloud (VPC).
* [ ] It provisions a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.
* [ ] It allows you to create a subsection of a virtual private cloud (VPC) where you can isolate resources and control access.
* [x] It translates human-readable domain names to machine readable IP addresses.

>[!NOTE]
>A DNS translates the domain name into your browser and sends it to a customer DNS resolver. It then asks the company DNS server for the IP address and returns it so the user can reach the website.

A customer is exploring edge networking services to improve application availability, performance, and security. They need a solution for traffic routing when something goes wrong in one of their application's locations. Specifically, it takes into account the endpoint health, user location, and policies.

Which AWS solution would BEST meet their needs?

* [ ] AWS Global Accelerator
* [ ] AWS Direct Connect
* [ ] Amazon CloudFront
* [ ] Amazon Route 53

A customer is exploring solutions to establish secure, encrypted connections between their on-premises networks at their data centers and branch offices. They are looking for the MOST cost-effective way to connect their office sites to other sites and their AWS services. They are not looking to increase the amount of bandwidth.

Which solution would BEST meet their needs?

* [ ] AWS Direct Connect
* [ ] AWS Client VPN
* [x] AWS Site-to-Site VPN
* [ ] AWS PrivateLink

>[!NOTE]
>AWS Site-to-Site VPN creates a secure connection between your data center or branch offices and your AWS Cloud resources.



An enterprise customer just merged with another company and needs a way to quickly scale and provide a way for the new worldwide sales force to access their AWS resources. They want a fully managed service with advanced authentication for their new remote workers.

Which solution would BEST meet their needs?

* [ ] AWS Site-to-Site VPN
* [ ] AWS Direct Connect
* [x] AWS Client VPN
* [ ] AWS PrivateLink

>[!NOTE]
>Amazon Client VPN is a networking service you can use to connect your remote workers and on-premises networks to the cloud. It provides advanced authentication, and elastic and remote access in a fully managed service.

A customer is creating an Amazon VPC for their application. They want to create a private segment in the Amazon VPC so that resources launched can be isolated from users on the internet.

Which network component would BEST meet their needs?

* [x] A private subnet
* [ ] Either a public subnet or a private subnet would work
* [ ] A public subnet
* [ ] An Availability Zone instead of a subnet

>[!NOTE]
>A private subnet is a network segment within a Virtual Private Cloud (VPC) that does not have a direct route to the internet. This would meet their needs for the application.

A retail customer is hosting their application in an Amazon VPC and wants to configure traffic rules for the Amazon EC2 instances running in a public subnet. The application requires multiple rules to be defined at the instance level. 

Which solution or feature would meet their needs?

* [ ] Change the public subnet to a private subnet to avoid public internet access.
* [ ] Set up a virtual private gateway based on the application requirements.
* [x] Set up security groups for the Amazon EC2 instances based on the application requirements.
* [ ] Set up network access control lists, (network ACLs) for the Amazon EC2 instances based on the application requirements.

>[!NOTE]
>Security groups would allow the fine-grained control at the instance level. They can define rules in the public subnet for the individual instances.


What is networking in the AWS Cloud?

* [ ] Physically isolated data centers or set of data centers within an AWS Region
* [ ] System that translates readable domain names to IP addresses
* [x] Interconnected devices that can exchange data and resources
* [ ] Logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define

>[!NOTE]
>You can think of networking in the AWS Cloud as the infrastructure and services working together to host your applications, data, and any other resources you might need.


A financial customer needs a content delivery solution to deliver required training videos and static content to their financial consultants worldwide. They want to make sure the solution provides low latency.

Which AWS solution would BEST meet their needs?

* [ ] AWS Global Accelerator
* [ ] AWS Direct Connect
* [ ] Amazon Route 53
* [x] Amazon CloudFront

>[!NOTE]
>CloudFront speeds up distribution of your static and dynamic web content to your users. It securely delivers your content with low latency through a worldwide network of data centers called edge locations.

A company wants to establish a secure, private connection between their on-premises data center and their Amazon VPC to create a hybrid cloud architecture.

Which component should they use to help ensure a secure connection?

* [x] Virtual private gateway
* [ ] Subnet
* [ ] Route table
* [ ] Internet gateway

>[!NOTE]
>A virtual private gateway is the virtual private network (VPN) endpoint on the AWS side. It provides a way for you to establish a secure, encrypted connection between your on-premises network and your virtual private cloud (VPC).

A customer is creating their application resources in their virtual private cloud (VPC) subnets. They want to secure their resources in the cloud, specifically the networking traffic protection tasks.

Which component is the customer responsible for, based on the shared responsibility model?

* [ ] Securing the hardware that runs the AWS Cloud services
* [x] Securing network traffic with the subnets and resources with Network access control lists (network ACLs) and security groups
* [ ] Securing access to the AWS data centers and facilities that run AWS Cloud services
* [ ] Securing the software that runs the AWS Cloud services

>[!NOTE]
>The customer is responsible for securing the network traffic. They can do this using security groups and network ACLs.

A media company needs a service to manage their domain registrations with different providers. They will also be using the service to route internet traffic to their resources hosted both in the AWS Cloud and elsewhere.

Which AWS solution would BEST meet their needs?

* [ ] AWS Global Accelerator
* [ ] AWS Direct Connect
* [x] Amazon Route 53
* [ ] Amazon CloudFront

>[!NOTE]
>Route 53 is a domain name system (DNS) service that manages domain registration, DNS routing, and health checks. It provides reliable and efficient routing of users to your website or applications, whether they are hosted within AWS or elsewhere.

A customer wants a way to establish a dedicated connection from their on-premises network to an Amazon VPC. They need a solution that provides a more consistent network experience with increased bandwidth.

Which type of connection to the AWS Cloud would BEST meet their needs?

* [ ] Internet gateway
* [x] AWS Direct Connect
* [ ] Amazon CloudFront
* [ ] Virtual private gateway

>[!NOTE]
>Direct Connect would establish a dedicated connection from an on-premises network to one or more virtual private clouds (VPCs). It can also reduce network costs, increase bandwidth throughput, and provide a more consistent network experience than internet-based connections.

What is the primary function of an Availability Zone in the AWS Cloud?

* [ ] It filters inbound and outbound traffic to EC2 instances in a VPC.
* [ ] It allows you to create a subsection of a virtual private cloud (VPC) where you can isolate resources and control access.
* [ ] It provisions a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.
* [x] It enhances application availability and fault tolerance by allowing resources to be deployed across multiple zones.

>[!NOTE]
>An Availability Zone is a physically isolated data center or set of data centers within an AWS Region. Each AZ has independent power, cooling, and networking, designed to enhance application availability and fault tolerance by allowing resources to be deployed across multiple Availability Zones within the same Region.


A customer is moving their application to an Amazon VPC and wants to setup a traffic control at the subnet level. They need broad control of traffic in and out and would like to use both allow and deny type rules.

Which solution or feature would meet their needs?

* [ ] Change the public subnet to a private subnet to avoid public internet access.
* [ ] Use security groups.
* [ ] Set up a virtual private gateway based on the application requirements.
* [ ] Use network access control lists (network ACLs).

>[!NOTE]
>Network ACLs would allow the broad traffic control at the subnet level. Network ACLs also have both allow and deny type rules.

