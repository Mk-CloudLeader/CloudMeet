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
