# AWS Partner: Accreditation (Technical)

## Background info: 
* Before cloud services companies has their own data centers that has resources and physically components like servers
* Now: we have cloud

## What is cloud computing? 
* Cloud computing refers to on-demand resouces delivery through internet
* resources include: compute, storage, database, applications, etc.

## What are the benifits of cloud computing? 
* Agiltiy --> easily assecible resouces at any time
* Elasticity --> scale up or down on resouces depending on need (automatically)
* Cost saving -->  save on buying physically components amd building for data center
* Deploy globally in minutes → cloud providers have infra all around the world 

## AWS global cloud infrastructure 
* aws cloud can deploy resources globally
* aws services allow users to implement redundancy
    * redundancy --> duplication/replication of something
    * fault tolerance 
  ### How does cloud do this?
  * Regions: cluster of AZs
  * Availability zones: cluster of data centers
  * Edge locations: global location where data is cached
    ** currently +400 locations 
    ** CloudFront??

## AWS core technology? 
* Aws provide resources for: compute, storage, database, security, management, and networking 

  ### Compute --> EC2
* EC2 is an AWS service that provides computing services, as it supply user with virtual instances(VMs) 

  ### Storage --> S3 and Elastic Block Store(EBS)
* What is S3?
  * It is an object level storage
    * piece of data is treated as a separate object
  * Stores data in resources called bucket
  * Common use is → as data lake, backup and storage, app hosting, software hosting, media hosting
  * Data lake → entralized repository, stores raw data
  * Ustructured so stores everything
* What is EBS?
  * It is block level storage
  * fixed-sized blocks
  * Hard drive of EC2 instances 


  ### Database --> RDS, DynamoDB, ElastiCache 
  ### Security --> IAM
  ### Management
  ### Networking --> VPC, Route 53
  

# AWS Technical Essentials (PART 2)

## Overview 
### Module 1: AWS services 

* What is cloud computing
   * on-demand deleviery of IT resources over internet
   * companies don't have to mantaine their own hardware and data centers
   * TYPE OF DEPLOYMENT METHOD:
      * on-premise
      * cloud
      * hybrid
    
* Advantages of cloud
   * Pay-as-you-go
   * speed/agility
   * cost saving
   * go global in mins
   
*  AWS global infrastructure
   * Redundant resources: which means duplicated for disaster recovery, hence available any time
   * Availability Zone: Cluster of data centers, data is replicated around multiple AZs
   * Region: Cluster of AZs
   * Edge network: caching data (see above for more info)

* AWS security
   * security is shared reponsiblity of user and aws
   * PICTURE

* AWS IAM (Identity Access and Management)
   * authentication:  "you are who you say you are"
   * authorization: "what actions can you perform" --> permission to take specific action
   * IAM:
      * manages access to AWS accounts and resources
      * checks who is allowed?
      * checks what can they do?
      * users can define who and what can use the resources  

### Module 2: AWS Compute

### Module 3: AWS Networking

### Module 4: AWS Storage


### Module 5: AWS Databases
* What is a database?
   *  Structured collection of data
   *  A centralized repository that allows multiple users and application to access data
   *  Simple terms ⇒ stores collection of data

* What is structured and unstructed database?
   * structured
      * Organized in columns and rows
      * In structured way
      * For instance: structured data included customer ID, name, address, phone number, and email as a column and each row has details for each column
   * unstructrured
      * opposite of structured
      * No structure
      * Examples: text documents, emails, social media posts, audio and video files, images, opinions comments etc.
      
* What is relational database? RDBMS 
   *  It is database management system
   *  This is a structured database as it manages and organizes data in tabular form consisting of rows and columns.
   
* What is SQL?
   *  Structured Query Language
   *  a programming language
   *  Structured → analyzing structured data
   *  SQL database refers to: RDBMS

* What is NoSQL?
   * Is also known as NoSQL database
   * Unlike traditional relational database which is structured, NoSQL focuses on unstructured data provides a different approach to storing and retrieving data
 
* What is OLTP?
   * Online Transaction Processing
   * Type of a database system
   * Handle and process high volumes of real-time transactions
   * RDS:
      * AWS relational database is based on OLTP     

* What is OLAP?
   * Online Analytical Processing
    
* What is caching?
   * in memory caching
   * The purpose of caching is to improve performance and reduce the need to fetch the data from the original source repeatedly.
   * hardware or software component that stores frequently accessed data or instructions in a quickly accessible location.
   * Reducing the time and effort required to access data from the main storage or memory.
   * keeping a copy of this frequently accessed data
   * providing faster access to frequently used data or instructions
 
* Amazon's DynamoDB?
   * No relational database
   * DynamoDB is a fully managed, highly available and scalable NoSQL database
   * Automatically and synchronously replicates data across AZ

### Module 6: Montoring









  |Ref| https://github.com/jvidalgz/aws-certified-solutions-architect-associate-notes/blob/master/README.md|
