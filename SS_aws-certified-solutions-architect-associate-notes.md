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

#Getting Started with AWS Storage
##Overview
* Storage Options
* Type of Storage: Block, File, Object
* Why move storage to cloud?

### Storage
* Data is one of the most important assest of a business, and data is stored in storage
* There are three types of primary storage: block, file, object
* First understand these types

### Types of storage
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/d7d21c86-0c0c-407c-97b9-f462607f617f)
* FILE:
   * in hierarchy structure
   * organized into folders and subfolders
   * simple/easy/cheap
* BLOCK:
   * large structured files like databases, application, OS
   * divided into blocks each with unique IDs
   * complex than file storage
* OBJECT:
   * new technology
   * for large unstructured data
   * useful for storing static content: movies, videos, songs, pictures, etc.     


#Amazon DynamoDB for Serverless Architectures
## Overview
* DynamoDB
* NoSQL
* Serverless Architecture
* core DynamoDB components and how-to setup and access them in creating a serverless application

### What is dynamoDB? 
* NoSQL database service that is designed for OLTP
* Also to note: it is a serverless database 
* does not use traditional rows and columns process to store data, like in relational database
* instead uses key-value, which means data is accessed by the primary key

If I were to sell dynamoDB to you I would tell you that is it:
*Fully Managed Service
* highly scalable
* global
* easily accessible and
* highly available 

### Understanding avability zones and replica
* Availability Zone: Cluster of data centers, and data is replicated around multiple AZs
* Now most business will have multiple data center, in case of disaster
   * Multi-region replication:
      * a feature that allows data to be replicated and synchronized across multiple regions in a distributed system
      * features: improved data availability, disaster recovery, and reduced latency for users in different geographic locations
important to understand because most cloud providers have this feature
## Explain the process of replica?    

### Understanding back up and restore
*  Now since you have these replicas of databases in different zones, backup and restore is easy
*  backup is created asynchronously, so not simultaneous  


### Caching 
* DAX is a DynamoDB-compatible caching service
* now what is caching? 
   * The purpose of caching is to improve performance and reduce the need to fetch the data from the original source repeatedly.
   * hardware or software component that stores frequently accessed data or instructions in a quickly accessible location.
   * reducing the time and effort required to access data from the main storage or memory.
   * keeping a copy of this frequently accessed data
   * providing faster access to frequently used data or instructions






