Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple resources, such as EC2 instances, to optimize performance and reliability. A load balancer serves as the single point of contact for all incoming web traffic to an Auto Scaling group. As the number of EC2 instances fluctuates in response to traffic demands, incoming requests are first directed to the load balancer. From there, the traffic is distributed evenly across the available instances.

Although ELB and Amazon EC2 Auto Scaling are distinct services, they work in tandem to enhance application performance and ensure high availability. Together, they enable applications running on Amazon EC2 to scale effectively while maintaining consistent performance.

### Key takeaways: ELB benefits

Let's review the main benefits of elastic load balancing and how it enhances the performance, scalability, and management of your AWS environment. To learn more, choose each of the following flashcards.

**Efficient traffic distribution:**  
ELB evenly distributes traffic across EC2 instances, preventing overload on any single instance and optimizing resource utilization.

**Automatic scaling:** 
ELB scales with traffic and automatically adjusts to changes in demand for a seamless operation as backend instances are added or removed.

**Simplified management:**
ELB decouples front-end and backend tiers and reduces manual synchronization. It also handles maintenance, updates, and failover to ease operational overhead.

### Routing methods

To optimize traffic distribution, ELB uses several routing methods: Round Robin, Least Connections, IP Hash, and Least Response Time. These routing strategies work together for efficient traffic management and optimal application performance.

**Round Robin**  
Distributes traffic evenly across all available servers in a cyclic manner.

**Least Connections**  
Routes traffic to the server with the fewest active connections, maintaining a balanced load.

**IP Hash**
Uses the client’s IP address to consistently route traffic to the same server.

**Least Response Time**  
Directs traffic to the server with the fastest response time, minimizing latency.

### Example: Elastic Load Balancing

Let's look at an example to better understand how Elastic Load Balancing works in cloud computing. In the healthcare industry, particularly in hospitals and medical facilities that provide online appointment booking systems or patient portals, website traffic can vary greatly throughout the day.

**Initial SetUp**
**Low-demand period**: At the beginning of the day, only a few patients are accessing the system to book appointments or view medical records. The existing web servers are sufficient to handle the low traffic. This matches the demand, with no need for additional resources at this point.

**Scaling Up**
**High-demand period**: As the day progresses, especially during peak hours, such as early mornings or just before the weekend, more patients access the portal to book appointments, view test results, or contact medical professionals. To handle this surge in demand, the healthcare system automatically scales up the number of servers to help ensure that the system remains responsive and available for all users.

**Load Balancing**
A load balancer directs the incoming traffic to different web servers based on their current load. For instance, if one server starts receiving too many requests, the load balancer will route new requests to a less busy server. This makes sure that no single server becomes overwhelmed. The traffic is evenly distributed across available EC2 instances.

By using Elastic Load Balancing and Auto Scaling, the healthcare industry can efficiently manage the varying levels of patient traffic to online services. This provides reliable access to medical portals even during high-demand periods.