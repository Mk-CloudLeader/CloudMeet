## Module 1: COMPUTE
### Background info: 
* Before cloud services companies has their own data centers that has resources and physically components like servers
* Now: we have cloud

### What is cloud computing? 
* on-demand deleviery of IT resources over internet
* companies don't have to mantaine their own hardware and data centers
* TYPE OF DEPLOYMENT METHOD:
   * on-premise
   * cloud
   * hybrid
* Cloud computing refers to on-demand resouces delivery through internet
* resources include: compute, storage, database, applications, etc.

### What are the benifits of cloud computing? 
* Agiltiy --> easily assecible resouces at any time
* Elasticity --> scale up or down on resouces depending on need (automatically)
* Cost saving -->  save on buying physically components amd building for data center
* Deploy globally in minutes → cloud providers have infra all around the world

### AWS global cloud infrastructure 
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
    
### Understanding cloud concepts
* DR: disaster recovery, in case of disaster cloud provides disaster recovery so user data is not lost 
* Regions: collection of multiple avalibity zones
* AZ: collection of multiple data centers
* Edge location: global location where data is cached, Content delivery network (CDN), cloud front
* Avalibity: availability at high speed, resources are available whenever users need it.
* Scalibility: users can configure auto-scaling to scale resource up/or down depending on need.

### AWS core technology? 
* Aws provide resources for: compute, storage, database, security, management, and networking 

### Compute --> EC2
* EC2 is an AWS service that provides computing services, as it supply user with virtual instances
* provides compute capacity in cloud
* provisons virtual servers called EC2 Instances
* Pay as you go service
* Scalable
* AWS Command Line (CLI): is a unified tool to manage your AWS services.
  * text based user interface --> manage files and run programs
  * manage services on ur device
 
*Gui*: graphical user interface, interface btween graphical icon and electronic device on ur computer  

### Serverless vs server-based 
* serverless --> computing model where cloud provider manages the infrastructure, scaling, and maintenance of the servers.
  * AWS lambda: serverless compute option provided by aws web service, that is automated by aws and users pay only of whatever is used to run their code
  * servers are deployed automatically in response to an event, for temporary time and then terminate after use
  * users only pay for what the used rather than entire server capacity 
* server based --> managing vms or servers where users have full control over the management of the infra but requires more time and effort
  
### What does it mean by virtualized server? 
* **Virtual machines** or virtual servers are computing option that allow user to deploy multiple OS on a single server
* Through **hypervisor**, which allows virtualization of hardware, users can create mutliple VMs on a single server
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/65921293-97ac-4674-8645-25447a6894da)

* **Containers** are also another computing option, that allows software and hardware componets needed for an application to run
* Through installation of a docker on an OS, multiple containers could run on that platform
* **Docker** allows virtualization of software
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/bc221778-1b68-44e0-b37f-30eccac87a38)

### Why virtualization through cloud instead of on-premise instances? 
* Scalibilty
* Pay-as-you-go
* speed/agility
* cost saving
* go global in mins

### AWS global infrastructure
* Redundant resources: which means duplicated for disaster recovery, hence available any time
* Availability Zone: Cluster of data centers, data is replicated around multiple AZs
* Region: Cluster of AZs
* Edge network: caching data (see above for more info)

### EC2 use case
* A company launches an e-commerce website during the holiday season. They use EC2 instances to handle the increased web traffic, ensuring that their website remains responsive and able to handle the influx of customers.
* Through EC2 companies can automate the amount of instances scalibility and pay only for what they use, saving time and money

### On-premise 
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/fad8b7da-a4d8-48ae-b5db-6623a8af6f7e)

### EC2 instance configuration 
* AMI image: OS
* CPU/Memory: Instance type
* Network: IP, Subnets, VPC
* Storage
* Security: NACL, security groups
* Key pair configuration: public key , private key
  * private key: private, securly kept on the local machine 
  * public key: openly shared key with others, stored on ec2 instance 

### Iaas, Saas, PaaS
* Infrastructure as a Service
  * EC2
  * where infrastruture like:  virtual machines, storage, and networking is provided as a service but user users are responsible for the OS running in the vms.
  * user responsible for managing and maintaining the software and applications  
* Software as a Service
  * software applications over the internet, so software is provided as a service
  * Microsoft 365
  * Upgrades, maintenance, and security of software is handled by the provider
* Platform as a Service
???
 
## Module 2: STORAGE
### Overview
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
   * Network-Attached Storage (NAS) - A storage solution that enables multiple users to seamlessly access and interact with files stored within a network.
   * in hierarchy structure
   * organized into folders and subfolders
   * simple/easy/cheap
* BLOCK:
   * large structured files like databases, applications, OS
   * divided into blocks each with unique IDs
   * complex than file storage
* OBJECT:
   * new technology
   * for large unstructured data
   * useful for storing static content: movies, videos, songs, pictures, etc.
  
### Amazon Simple Storage Service (Amazon S3):
  * It is an object level storage
    * piece of data is treated as a separate object
  * Stores data in resources called bucket
  * Common use is → as data lake, backup and storage, app hosting, software hosting, media hosting
  * Data lake → entralized repository, stores raw data
  * Ustructured so stores everything
### Amazon Elastic Block Store (Amazon EBS):
  * It is block level storage
  * You can think of EBS as a cloud-based virtual hard disk.
  * Each EBS volume is automatically replicated within its Availability Zone to protect from both component failure and disaster recovery 
  * fixed-sized blocks
  * Hard drive of EC2 instances

### SSD vs HDD are two types of block storage 
* SSD: transactional workload
* HDD: large streaming workloads

### Amazon Elastic File System (Amazon EFS):
* simple and fully managed elastic NFS file system
* automatically and instantly scales file system storage capacity up or down as user add or remove files without disrupting your application.

## Module 3: DATABASE
### What is a database?
   *  Structured collection of data
   *  A centralized repository that allows multiple users and application to access data
   *  Simple terms ⇒ stores collection of data

### What is structured and unstructed database?
   * structured
      * Organized in columns and rows
      * In structured way
      * For instance: structured data included customer ID, name, address, phone number, and email as a column and each row has details for each column
   * unstructrured
      * opposite of structured
      * No structure
      * Examples: text documents, emails, social media posts, audio and video files, images, opinions comments etc.
      
### What is relational database? RDBMS 
   *  It is database management system
   *  This is a structured database as it manages and organizes data in tabular form consisting of rows and columns.
   
### What is SQL?
   *  Structured Query Language
   *  a programming language
   *  Structured → analyzing structured data
   *  SQL database refers to: RDBMS

### What is NoSQL?
   * Is also known as NoSQL database
   * Unlike traditional relational database which is structured, NoSQL focuses on unstructured data provides a different approach to storing and retrieving data
 
### What is OLTP?
   * Online Transaction Processing
   * Type of a database system
   * Handle and process high volumes of real-time transactions
   * RDS:
      * AWS relational database is based on OLTP
   
### What is OLAP?
   * Online Analytical Processing
    
### What is caching?
   * in memory caching
   * The purpose of caching is to improve performance and reduce the need to fetch the data from the original source repeatedly.
   * hardware or software component that stores frequently accessed data or instructions in a quickly accessible location.
   * Reducing the time and effort required to access data from the main storage or memory.
   * keeping a copy of this frequently accessed data
   * providing faster access to frequently used data or instructions
 
### Amazon's DynamoDB?
   * No relational database
   * DynamoDB is a fully managed, highly available and scalable NoSQL database
   * Automatically and synchronously replicates data across AZ

### Metadata
   * information about other data
   * file name, size, creation date, author, tags, location etc.
### ledger database
   * blockchain platforms like Bitcoin
   * database designed specifically for recording and maintaining a transparent and tamper-proof history of transactions or events

### Backup and recovery
   * involve creating copies of data and implementing strategies to restore that data in case of accidental deletion, data corruption, hardware failures, natural disasters, or other catastrophic events.

### Databases: 
* MongoDB
   * NoSQL document database
* Cassandra
   * highly scalable and distributed NoSQL database 
* Dynambo DB
   * Amazon DynamoDB is a fully managed NoSQL database service provided by Amazon Web Services (AWS).
 
# Amazon DynamoDB for Serverless Architectures
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

### Cloud database from aws 
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
### Asynchronous replication
* write data to the primary storage first and then copy the data to the replica.
### Synchronous replication 
* write data to primary storage and the replica simultaneously

### Understanding back up and restore
*  Now since you have these replicas of databases in different zones, backup and restore is easy
*  backup is created asynchronously, so not simultaneous  

### What is RDS?
* fully managed service for running relational databases on AWS
* supports six different database engine including: MySQL, PostgreSQL, and MariaDB (all open source)
     
## Module 4: MONITORING
### Five step plan to migrating from MySQL to Amazon RDS? 
* create MySQL database instance on AWS RDS
   * video of how to do it
   * some things they mentioned to configure: engine type you would use MySQL, mention storage you would use
* create a replication instance in AWS DMS (databse migration service)
   *  
* create source and target endpoints for your database migration
   *  
* create a replication task in DMS
   * 
* complete the migration and clean up the resources
   * 
## Module 5: NETWORKING
# VPC
### What is networking? 
* Connecting computing devices with each other for communication

### What’s the need of private network? 
* Is it possible for a company to grant all of its resource rights to the public? NO.
* Private cloud is a method of sharing resources exclusively within a company's network.

### What is vpc? (Virtual private cloud)
* virtual data center in cloud
* It is a virtual private cloud
* allows users to create a private network within cloud environment 
* It is basically a fully customizable network

### Why would one need a private cloud?
* Companies have a public cloud that allows public to access certain resources
* but would company give all resource rights to public? NO
* private cloud is used for sharing resources privately among company
* a private cloud is like having your own personal section of the cloud, reserved exclusively for your organization's use

### What is possible with VPC?
* Create an isolated virtual network
* Customize the network
   * full control over: IP address ranges, subnets, route tables, internet gateway and security settings.
* High level security

### Components of VPC network:
* IP address ranges
   * determines the number of IP addresses available for your resources within the VPC
* Subnets
   * To divide your network in chunks
   * You need subnets because it allows resources to be broken into managble fragments 
   * Public and private
* Route tables
   * Determines traffic flow of network within the VPC
* Internet gateway
   * Allow connection with public subnets and your VPC
* NAT gateway
   * For private subnets
   * Allowing private subnets access to the internet
* Security settings
   * NACL (subnet level):network access control lists: act as a firewall at the subnet level, managing inbound outbound traffic
   * Security groups (instance level): same at NACL, except they work at instance level, they control inbound and outbound traffic for individual instances

## Security groups:
* secure access to your individual EC2 instances
* Acts as a firewall for each instance
* Controlling the inbound and outbound traffic for network flow

## NACL
* Same as security groups, in terms that it also acts as a fire wall
* But for subnet level!
* They act as a firewall for all instances in subnet level, rather than working for individual instance
* Although they are similar to security groups major difference
   * NACL → stateless
   * Security groups → stateful 

## Subnets 
* What are subnets?
   * It is a division of IP networks allowing managmeble groups of devices within a larger network
   * It is a network inside a network 
* Beneifts of subnetting?
   * Improve security
   * Improve perfomramce
   * Improve managebilty 
* Subnet mask
   * Each subnet has it unique host ID
   
## Route tables 
* Used by routers to determine the best paths of data 

## Gateways 
* Bridges or interface
* entry or exit point between two different networks
* Two types: Internet and NAT
   * Internet → allows internet access to public subnets
   * NAT → allows internet access to private subnets 

## AWS cloud front
* Is CDN → or content delivery network
* Through edge locations cloud front  deliver content with high speed
* Edge locations → data center locations in world that strategically placed around the world to bring content closer to end-users
* Cloud front is used for caching data from edge locations closer to user when user makes a request 

# AWS services 
## AWS Private link: private connection between your VPCs and services
* Without internet need
* a direct network connection established between two endpoints

## VPC peering 
* Networking connection between two VPCs
* Private 

## AWS Global accelerator
* Accelerator as in accelerates availability and performance of applications running in multiple AWS Regions

# Route 53
* What is Route 53?
   * It is DNS --> Domain name system
   * Provided by AWS
* What is DNS?
   * decentralized naming system used to translate domain names (e.g., www.example.com) into IP addresses (e.g., 192.0.2.1).
   * allows users to access websites and other resources using memorable domain names instead of numerical IP addresses.

* AWS IAM (Identity Access and Management)
   * authentication:  "you are who you say you are"
   * authorization: "what actions can you perform" --> permission to take specific action
  
  ### IAM:
     * Identity access management
     * allows one to configure roles on what users can access
     * it creates user id and grants permission to those users
     * Create groups and roles
     * it is a way to grant access to aws resources
      * manages access to AWS accounts and resources
      * checks who is allowed?
      * checks what can they do?
      * users can define who and what can use the resources
  ## start of iam
  * Starts with a **root account** which is the email address used to sign up to aws
  * IAM allows company to manage 
    * Users: user who need access to aws resources in a company
    * Groups: collection of users; Groups allow you to specify permissions for similar types of users. 
    * Roles: IAM roles are used by AWS services to access other AWS resources ; giving temporary access to resource 
    * Policies: define permission 
    * Permissions: actions are allowed or denied 
    * Authentication and Authorization: authentication (ensuring users are who they claim to be) and authorization (determining what actions a user is allowed to perform).
## Types of AWS Credentials
* Password/username: allowing user to access through username and password created at the aws account
* Multi-factor authentication: additional layer of security -->  more than one authentication factor is checked before access is granted, which consists of a user name and password, and the single-use code
* user access key

### AWS Tech topics: 
# AWS Auto Scaling
* What is auto scaling?
   *  adjusting resources based of user demand, automatically
   *  so example: you have 5 server working for tik tok right now, and there are only 10 users so the servers are good, but suddenly you see a splurge in users and users start feeling latency in the videos that they get. this is bc the workload on servers have reached max capacity, you need to manaully add more servers, which could again experience same problem. So companies rely on auto scaling for all their resources.

# Load Balancer
### Overview
* What is a load balancer?
* What are types of load balancer?

#### What is a load balancer? 
* device that helps distribute network traffic evenly across multiple servers/resources
* purpose: prevent a single server from becoming overwhelmed with too much traffic
* purpose: and to ensure workload is evenly distributed among other servers to prevent servers crash
  
### To create a load balancer one needs?
* Protocol listerners
* Target types
* Load Balancer Type and Configuration (OSI model layer)

### What is OSI model layer?
* 
we are focusing on aws Elastic Load balancer, which provides three types of load balancers to distribute traffic across Amazon EC2 instances and other AWS resources. These three types are:
## Classic Load Balancer (CLB):
* Operates at both Layer 4 (Transport Layer) and Layer 7 (Application Layer).
## Application Load Balancer (ALB):
* Operates at Layer 7 (Application Layer) of the OSI model.
## Network Load Balancer (NLB)
* Operates at Layer 4 (Transport Layer) of the OSI model.

#### Add notes to IAM and add to load balancer more notes 
notes not added yet: IAM, IAM roles, encryptions 

