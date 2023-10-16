
### Architecture of API Gateway
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/5b6714d7-65d0-45b7-abf4-900ea9910b0f)

- Amazon API Gateway is an AWS service for creating, publishing, maintaining, monitoring, and securing **REST, HTTP, and WebSocket** APIs at any scale.
- Amazon API Gateway helps developers to create and manage APIs to **back-end systems** running on Amazon EC2, AWS Lambda, or any publicly addressable web service. With Amazon API Gateway, you can generate custom client SDKs for your APIs, to connect your back-end systems to mobile, web, and server applications or services.

  - Choose an API type [ Four diffent types in AWS]
    
         - HTTP  : Build low-latency and cost-effective REST APIs with built-in features such as OIDC and OAuth2, and native CORS support.
         - WebSocket API :Build a WebSocket API using persistent connections for real-time use cases such as chat applications or dashboards.
         - REST API : Develop a REST API where you gain complete control over the request and response along with API management capabilities
         - REST API <Private> : Create a REST API that is only accessible from within a VPC.

    ![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/0c754057-d3d3-481d-bef8-d2fe5c2367bc)

- API Gateway creates RESTful APIs that: 

    - HTTP  : Build low-latency and cost-effective REST APIs with built-in features such as OIDC and OAuth2, and native CORS support.
      
     - Are HTTP-based.
     - Enable stateless client-server communication.
     - Implement standard HTTP methods such as GET, POST, PUT, PATCH, and DELETE.

### Use case- 01

  For an app to call publicly available AWS services, you can use Lambda to interact with required services and expose Lambda functions through API methods in 
  API Gateway. AWS Lambda runs your code on a highly available computing infrastructure. It performs the necessary execution and administration of computing 
  resources. To enable serverless applications, API Gateway supports streamlined proxy integrations with AWS Lambda and HTTP endpoints.

- As I explained how I integrated **Snowflake** with **AWS SES** using API and Lambda Function. Snowflake uses AWS SES to send notification using API, backend Lambda.  




### Reference :   
 | AWS API Gateway | https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html |
 |Tutorial: Build an API Gateway REST API with cross-account Lambda proxy integration | https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-cross-account-lambda-integrations.html|
 
 |Serverless Developer Guide| https://docs.aws.amazon.com/serverless/latest/devguide/welcome.html |
 | workshop| https://catalog.workshops.aws/serverless-patterns/en-US/business-scenario|
 
 
 
