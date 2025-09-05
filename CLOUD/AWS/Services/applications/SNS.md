Amazon SNS is a publish-subscribe service that publishers use to send messages to subscribers through SNS topics. In Amazon SNS, subscribers can include web servers, email addresses, Lambda functions, and various other endpoints. You will learn about Lambda in more detail later.

### Example: Amazon SNS

A company that sells a variety of products is currently sending a single email to all customers with updates on various topics, such as new products, special offers, and upcoming events. Although this method worked initially, customers want to receive only the updates they’re interested in. The current email update is causing customer dissatisfaction and lower engagement.

To learn more about the solution, choose each of the three numbered markers.

1. **Segment the communication**

The company decides to divide the communication into three separate topics, including one for new products, one for special offers, and one for events. Each topic will focus on a specific area of interest.

2. **Let customers choose topics**

Customers can subscribe to the topics they care about, such as the following:

- A customer might subscribe only to new product updates.
- Another customer might opt only for event notifications.
- A third customer might choose to subscribe to new product updates and special offers.

3. **Send tailored notifications**

With Amazon SNS, the company can send personalized notifications to subscribers based on their specific interests. Amazon SNS makes sure that these notifications are promptly delivered to the right audience, improving the efficiency and relevance of the communication.

