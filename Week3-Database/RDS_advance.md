--------------------
## Strategies and best practices for very large database migrations into Amazon RDS for Oracle
https://aws.amazon.com/blogs/database/strategies-and-best-practices-for-very-large-database-migrations-into-amazon-rds-for-oracle/

## Upgrading a DB instance engine version
## Upgrading the PostgreSQL DB engine for Amazon RDS

**Use case** : Amazon RDS for PostgreSQL minor versions 14.4, 14.3, 13.7, 12.11 and 11.16 will reach end of standard support on September 25, 2023. We recommend that you take action and upgrade your RDS for PostgreSQL databases running minor versions 14.4, 14.3, 13.7, 12.11 or 11.16 to versions 14.8, 13.11, 12.15 and 11.20 or higher before September 25, 2023. 
Alternatively, you can enable Automatic Minor Version Upgrade to allow Amazon RDS to upgrade your instances. Starting August 25, 2023 00:00:01 AM UTC, you will not be able to create new RDS instances with PostgreSQL minor versions 14.4, 14.3, 13.7, 12.11 and 11.16 from either the AWS Console or the CLI. 

We recommend that you upgrade your databases before September 25, 2023. During a scheduled maintenance window between September 25, 2023 00:00:01 UTC and October 25, 2023 00:00:01 UTC, RDS will upgrade your PostgreSQL databases running minor versions 14.4, 14.3, 13.7, 12.11 and 11.16 as well as any instances restored from the snapshots of these versions to 14.8, 13.11, 12.15 and 11.20 or higher. 

On October 25, 2023 00:00:01 AM UTC, any PostgreSQL databases running minor versions listed above that remain will be upgraded to 14.8, 13.11, 12.15 and 11.20 or higher regardless of instances’ scheduled maintenance window

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.Upgrading.html#USER_UpgradeDBInstance.Upgrading.AutoMinorVersionUpgrades \

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.PostgreSQL.html


### There are two types of upgrades you can manage for your PostgreSQL database:
- Operating system updates
- Database engine upgrades


### The IP addresses of my DB instances aren't consistent? 
In Amazon RDS, the IP addresses are dynamic while the endpoints are static. Therefore, it's a best practice to use endpoints to connect to your instance. Every Amazon RDS instance has an endpoint.

**The IP addresses of my DB instances aren't consistent**
Because the IP address of your instance is dynamic, you can't assign a static IP address or an Elastic IP address to your instance. The IP address assigned to an RDS DB instance changes under one or more of the following conditions:

- The instance is stopped and started again.
Note: When the instance is rebooted, the IP addresses don't change.
- The underlying host is replaced because of circumstances such as instance failure and DB instance class update.
- A hardware maintenance happened on the instance.
- The instance is in a Multi-AZ environment, and a failover happened.
- The operating system of the DB instance undergoes software patching.
- A manual failover of the DB instance is initiated using a reboot with failover.
- The DB engine undergoes a major or minor version upgrade.
- There is an outage in the Availability Zone of the instance.





