### ELB vs. ALB vs. NLB: Choosing the Best AWS Load Balancer
-------------------------------------------------------------------------




![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/aa4c55a3-a8ba-491a-a8e0-7ed72a8ebb91)


Feature	Application Load Balancer	Network Load Balancer	Gateway Load Balancer	Classic Load Balancer
Load Balancer type	Layer 7	Layer 4	Layer 3 Gateway + Layer 4 Load Balancing	Layer 4/7
Target type	IP, Instance, Lambda	IP, Instance, Application Load Balancer	IP, Instance	 
Terminates flow/proxy behavior	Yes	Yes	No	Yes
Protocol listeners	HTTP, HTTPS, gRPC	TCP, UDP, TLS	IP	TCP, SSL/TLS, HTTP, HTTPS
Reachable via	VIP	VIP	Route table entry	 
Common configurations and characteristics				
Slow start	✔	 	 	 
Outpost support	✔	 	 	 
Local Zone	✔	 	 	 
IP address - Static, Elastic	 	✔	 	 
Connection draining (deregistration delay)	✔	✔	✔	✔
Configurable idle connection timeout	✔	 	 	✔
PrivateLink Support	 	✔ (TCP, TLS)	✔ (GWLBE)	 
Zonal Isolation	 	✔	✔	 
Session resumption	✔	✔	 	 
Long-lived TCP connection	 	✔	✔	 
Load Balancing to multiple ports on the same instance	✔	✔	✔	 
Load Balancer deletion protection	✔	✔	✔	 
Preserve Source IP address	✔	✔	✔	 
WebSockets	✔	✔	✔	 
Supported network/Platforms	VPC	VPC	VPC	EC2-Classic, VPC
Cross-zone Load Balancing	✔	✔	✔	✔
IAM Permissions(Resource, Tag based)	✔	✔	✔	✔ (Only resource based)
Flow Stickiness (All packets of a flow are sent to one target, and return traffic comes from same target)	Symmetric	Symmetric	Symmetric	Symmetric
Target Failure behavior	Fail close on targets, unless all targets are unhealthy(fail open)	Fail close on targets, unless all targets are unhealthy(fail open)	Existing flows continue to go to existing target appliances, new flows are rerouted to healthy target appliances.	 
Health Checks	HTTP, HTTPS, gRPC	TCP, HTTP, HTTPS	TCP, HTTP, HTTPS	TCP, SSL/TLS, HTTP, HTTPS
Security				
SSL Offloading	✔	✔	 	✔
Server Name Indication (SNI)	✔	✔	 	 
Back-end Server Encryption	✔	✔	 	✔
User Authentication	✔	 	 	 
Custom Security Policy	 	 	 	✔
ALPN	✔	✔	 	 
Kubernetes Controller				
Direct-to-pod	✔	✔ (Fargate pods)	 	 
Load Balance to multiple namespaces	✔	 	 	 
Support for fully private EKS clusters	✔	✔	 	 
Logging and monitoring				
CloudWatch Metrics	✔	✔	✔	✔
Logging	✔	✔	✔	✔
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/c606f20d-13dd-4501-b0b8-802e645bf9c5)


|ELB|  |https://aws.amazon.com/blogs/aws/category/elastic-load-balancing/|
|ALB|  |https://aws.amazon.com/blogs/aws/new-aws-application-load-balancer/|
|NLB|  | | |
|Best practices for deploying Gateway Load Balancer |     |https://aws.amazon.com/blogs/networking-and-content-delivery/best-practices-for-deploying-gateway-load-balancer/|
