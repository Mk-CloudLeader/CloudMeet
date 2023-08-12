## AWS_Elastic Compute Cloud (EC2)

### - EC2 Overview
### - Demo : Launching an EC2 Instance
### - AWS Command Line (CLI)
### - Using Roles
### - Security Groups & Bootstrap Scripts
### - Ec2 Metadata and User Data
### - Networking With EC2
### - Optimizing with EC2 Placement Groups
### - Solving Licensing Issue with Dedicated Hosts
### - Timing workload with Spot instances with Spot Fleets
### - Deploying vCenter in AWS with VMware Cloud on AWS
### - Extending AWS Beyond the cloud with AWS Outpost
### - LAB : EC2 Instance Bootstrapping
### - Lab: Using EC2 Roles and Instance Profiles in AWS
### - Q&A

## ------------------------
HA & Scalablity 
## -------------------------
- Horizontal Vs vertical scaling 
- launch template 
- ASG : Scalaing EC2 & Scaling policies  
- RDS & Non-RDS - Scaling 


### - EC2 Overview

![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/fdf4f880-4b31-4d7c-bf7c-56afc7a1459e)

**Physical to Virtual to container **
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/531852c4-db5a-491c-88bf-24d2e2778c84)


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
  - estimate the cost for your architectural solution
  - the different pricing models of EC2
     On-demand : Pay by hr or second based on instance family type 
     reserved   : reserved capacity for 1 - 3 years. upto 72% discount 
     Spot  : purchase unused capacity at discount of 90%. price fluctuates with supply and demand   
     Dedicated : A physical server dedicated for your use. Most expensive. <use case : compliance, Licensing)
                 Supports both on-demand and reserved 
        
      


| Link | https://aws.amazon.com/ec2/instance-types/|



### - Demo : Launching an EC2 Instance


### - AWS Command Line (CLI)

(AWS CLI) is a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts.

To check the currently installed version, use the following command:
$ aws --version

aws-cli/2.10.0 Python/3.11.2 Linux/4.14.133-113.105.amzn2.x86_64 botocore/1.13

- Secret Access Key – you will only see this once, and if you lose it, you need to delete the secret key ID & Secret access key and regenerate them. You need to run aws configure again on your server. 


| CLI Example | https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html  |


| CLI command reference | https://docs.aws.amazon.com/cli/latest/reference/#available-services |


### - Using Roles
- what is an IAM Role?
Roles are Temporary. AWS Identity and Access Management (IAM) roles are entities you create and assign specific permissions to that allow trusted identities such as workforce identities and applications, to perform actions in AWS. When your trusted identities assume IAM roles, they are granted only the permissions scoped by those IAM roles.
  ![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/28b186e3-ffe1-4e81-b599-c3aa4e253f70)
  Source : AWS document



  ![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/b9f77b3a-a870-4719-83ec-c4e8c507255d)


  
### Create first EC2
![image](https://github.com/Mk-CloudLeader/aws_Meetup-2023/assets/66654978/fe1efbda-e33a-4779-a345-02db78123474)


### Security Groups & Bootstrap Scripts

### Spot instances | Spot prices|Spot blocks |Spot fleets | use cases

- when do you use SPOT instances event 90% discounted rate?
   Stateless, fault-tolerant, or flexible application - Ex: Big data analysis, Containerlized workload, CI/Cd testing, Image & media rendering, HPC(high performance computing) 
  you can't use SPOT instance like to webserver or prod env.

- what is SPOT blocks?
- Use spot blocks to stop your SPOT instance from being terminated even if SPOT price goes above your max price. you can SPOT block 1-6 hrs only.
- you can see historical data of SPOT instance

### what is AWS Outpost?
- AWS DC at your on-prem. you can have Outpost in Size such as 1U & 2U servers and all way upto 42U racks and multiple rack deployments.
- Fully managed infrastructure
- family members - Outpsot rack , Outpost servers 



### High Availability  & Scalability 
- Horizontal Vs vertical scaling 
The 3 W's of Scaling - What(define template) --where (webserver or DB) --when  ( CW alarms can tell)
- what do we scale?
- where do we scale?
- when do we scale?


 ****Launch template Vs configuration 
 



