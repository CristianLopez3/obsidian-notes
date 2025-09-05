Lambda is a serverless compute service that runs code in response to events without the need to provision or manage servers. It automatically manages the underlying infrastructure, scaling resources based on the volume of requests. You are charged only for the compute time consumed, down to the millisecond. Lambda handles execution, scaling, and resource allocation. You can optimize performance by configuring the appropriate memory size for your function.

**How Lambda works**

## Upload code to Lambda

First, upload the code to Lambda, which uploads as a _Lambda function_.

## Set code to trigger from an event source

Next, configure your code to be triggered by events, like AWS services, mobile apps, or HTTP requests.

## Run code when triggered

Your code runs only when an event occurs, like a file upload or user action. Lambda automatically handles all the server management, scaling, and infrastructure. The Lambda runtime executes your function code using the event data passed to it. This way, your code runs reliably, securely, and efficiently—without you managing the servers or environment it runs in.

## Pay only for the compute time used

You are charged only for the compute time consumed, down to the millisecond. The price depends on the amount of memory that you allocate to your function.

# **Lambda use cases**

Lambda is ideal for building responsive, event-driven applications across a wide range of industries. Here are three real-world examples that show how Lambda helps companies scale efficiently, reduce operational overhead, and only pay for what they use.

### Real-time image processing for a social media application

A social media company uses Lambda to process images uploaded by users. When a photo is uploaded, Lambda is triggered to resize the image, apply filters, and save it in an optimized format to storage. This event-driven, serverless approach makes sure that the application can handle high volumes of uploads without needing to manage infrastructure.

  
**Why Lambda**: It automatically scales based on uploads and charges only for the time spent processing each image.

### Personalized content delivery for a news aggregator

A news aggregator uses Lambda to fetch and process news articles from multiple sources, then it tailors recommendations based on user preferences. When a user opens the application or performs a search, Lambda functions are triggered to retrieve data, run personalization logic, and return relevant content.

  
**Why Lambda**: It automatically scales with user traffic and reduces costs by running code only when users interact.


### Real-time event handling for an online game

A gaming company uses Lambda to handle in-game events like player actions, game state changes, and real-time leader board updates. Each event (like scoring a point or unlocking an achievement) triggers a Lambda function that updates player data and game status.

**Why Lambda**: It handles thousands of events, in real-time, with no need to manage servers. Costs scale with usage, which is ideal for peak gaming times.