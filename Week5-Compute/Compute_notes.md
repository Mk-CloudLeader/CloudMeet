# AWS_Elastic Compute Cloud (EC2)

## - EC2 Overview
## - Demo : Launching an EC2 Instance
## - AWS Command Line (CLI)
## - Using Roles
## - Security Groups & Bootstrap Scripts
## - Ec2 Metadata and User Data
## - Networking With EC2
## - Optimizing with EC2 Placement Groups
## - Solving Licensing Issue with Dedicated Hosts
## - Timing workload with Spot instances with Spot Fleets
## - Deploying vCenter in AWS with VMware Cloud on AWS
## - Extending AWS Beyond the cloud with AWS Outpost
## - LAB : EC2 Instance Bootstrapping
## - Lab: Using EC2 Roles and Instance Profiles in AWS
## - Q&A


### - EC2 Overview

![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/f0928bf2-bb68-4597-a782-510fc8c3321a)

- Secure resizable compute capacity in the cloud
- Like a VM, only hosted in AWS instead of your own data center 
- Designed to make a we- scale cloud computing easier for developers
- The capacity you want when you need it
- Cloud Compute Vs Datacenter VM


- **EC2 Pricing Options**

1. **On demand:**  Pay by the hour or the second, depending on the type of instance you run
- Flexible - low cost and flexibility of EC2 without any upfront payment or long term commitment 
- Short-Term- application with short term, a spiky, or unpredictable workloads that cannot be interrupted 


3. **Reserved capacity** for one or three years. Up to 70% discount on the hourly charge 

-	predictable usage - application with sturdy states or predictable usage 
-	 Pay upfront, you can make upfront payment to reduce to total computing cost even further
-	Standard RI's up to 70% of the on demand price
-	Convertible RIs,  up to 54% off the on demand price, has the option to change to different RI type of equal or greater value 
-	Scheduled RIs,  launch with the time window you define, match capacity reservations to predictable reoccurring schedule that only requires your fraction of day week or month 


4. **Spot** purchase unused capacity at the discount of up to 90%. Prices fluctuate with supply and demand

  - Use of Spot instance - 
       - Image rendering
       - generic sequencing
       - algorithm trading engines 

6. **Dedicated** A physical EC2 server dedicated for your use. The most expensive options 

- **Compliance**,  regulatory requirements that may not support multi tenant virtualization
- **Licensing**,  great for licensing that does not support multi tenancy or cloud deployments

- On demand , can be purchased on-demand hourly 
- Reserved can be purchased as a reservation for up to 70% of the on demand price  

**EC2  pricing calculator** 
  - estimate the cost for your architecture solution  


| Link | https://aws.amazon.com/ec2/instance-types/|



### - Demo : Launching an EC2 Instance


### - AWS Command Line (CLI)

### - Using Roles

