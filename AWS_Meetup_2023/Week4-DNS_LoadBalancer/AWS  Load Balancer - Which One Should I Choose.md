### ELB vs. ALB vs. NLB: Choosing the Best AWS Load Balancer
-------------------------------------------------------------------------


##	Application Load Balancer|	Network Load Balancer|	Gateway Load Balancer|	Classic Load Balancer

![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/c606f20d-13dd-4501-b0b8-802e645bf9c5)



![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/aa4c55a3-a8ba-491a-a8e0-7ed72a8ebb91)

**AWS provides** different load balancer services, including Elastic Load Balancer (ELB), Application Load Balancer (ALB), and Network Load Balancer (NLB). Below are breakdown of their differences and some recommendations:

-  **Elastic Load Balancer (ELB)**: ELB is the original load balancer service from AWS and is now known as Classic Load Balancer (CLB). It provides basic load balancing functionality at the transport layer (Layer 4) of the OSI model. ELB distributes traffic evenly across multiple instances and supports TCP and SSL/TLS protocols. However, it lacks advanced features and fine-grained control compared to ALB and NLB.

-  **Application Load Balancer (ALB)**: ALB operates at the application layer (Layer 7) and offers advanced routing capabilities. It provides content-based routing, SSL/TLS termination, and supports HTTP/HTTPS protocols. ALB allows you to route requests based on URL path, host headers, and HTTP methods. It also supports features like sticky sessions, request tracing, and server name indication (SNI). ALB is recommended for HTTP and HTTPS traffic routing and when you need advanced application-layer routing features.

 - **Network Load Balancer (NLB)**: NLB operates at the transport layer (Layer 4) and is designed for handling TCP, UDP, and TLS traffic. It provides ultra-low latency and high throughput, making it ideal for high-performance, latency-sensitive applications. NLB is useful for scenarios that require direct access to the IP addresses of the backend instances, such as in a container-based or microservices architecture. It also supports static IP addresses, preserving the client's source IP.

**Recommendations**:
- If you need basic load balancing functionality, you can consider using ELB/CLB. AWS discourages the use of ELB in favor of its newer load balancers. I would advice to use ALB or NLB that meet all customer requirements compare to ELB.

- For HTTP and HTTPS traffic with advanced routing requirements, ALB is a suitable choice.
- If you require high-performance, low-latency load balancing or need to preserve client source IP addresses, NLB is a good option.

The choice between ALB and NLB depends on your specific use case, traffic patterns, and requirements. It's also worth considering the cost implications and potential future scalability needs when selecting a load balancer service.

| Title  | Link |
| ------------- | ------------- |
| ELB |  https://aws.amazon.com/blogs/aws/category/elastic-load-balancing/ |
| ALB  |   https://aws.amazon.com/blogs/aws/new-aws-application-load-balancer/ |
| NLB |  xx  |
| Best practices for deploying Gateway Load Balancer      | https://aws.amazon.com/blogs/networking-and-content-delivery/best-practices-for-deploying-gateway-load-balancer/ |
|FAQ |  https://aws.amazon.com/elasticloadbalancing/faqs/ |
