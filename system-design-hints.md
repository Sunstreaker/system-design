# system-design-hints

## 𝐊𝐞𝐲 𝐒𝐭𝐫𝐚𝐭𝐞𝐠𝐢𝐞𝐬 𝐭𝐨 𝐁𝐨𝐨𝐬𝐭 𝐀𝐏𝐈 𝐏𝐞𝐫𝐟𝐨𝐫𝐦𝐚𝐧𝐜𝐞

* **Use Caching** - Store frequently accessed data in memory so you don’t have to fetch it from the database or other slow sources repeatedly. This drastically cuts down on response time.
* **Minimize Payload Size** - Send only the necessary data in responses. Avoid sending large, unneeded chunks of data by filtering fields or compressing the payload, which reduces bandwidth usage and speeds up responses.
* **Use Asynchronous Processing** - For tasks that don’t need an immediate response (like sending emails or processing large data sets), use asynchronous methods. This keeps the API responsive while the heavy work happens in the background.
* **Load Balancing**- Distribute incoming API requests across multiple servers to ensure no single server is overloaded. This improves availability and handles more traffic efficiently.
* **Optimize Data Formats** - Use lightweight data formats like JSON or Protocol Buffers instead of XML. Smaller data formats reduce the time spent parsing and transmitting data.
* **Connection Pooling** - Reuse existing connections to the database or other services rather than opening a new one for each request. Connection pooling significantly reduces the overhead of establishing connections.
* **Use Content Delivery Networks (CDNs)** - For APIs serving static content (like images or scripts), use CDNs to deliver content faster by caching it closer to the user’s location, reducing latency.
* **Implement API Gateway** - An API Gateway can help in routing requests, handling authentication, rate limiting, and caching. By offloading these tasks from your API, you can improve its overall performance.
* **Avoid Overfetching and Underfetching** - Design your API endpoints to return just the right amount of data. GraphQL, for example, allows clients to request exactly what they need, avoiding overfetching and underfetching issues common in REST APIs.

