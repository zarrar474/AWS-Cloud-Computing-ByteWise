# DynamoDB
## Resource
[DynamoDB](https://www.dynamodbguide.com/what-is-dynamo-db)

**DynamoDB is database by AWS, hosted NoSQL**
> Reliable scalable performance
> Managed Experience
> Smaal and Simple API

### Use Cases
> Apps with large amounts of data and strict latency requirment
> Serverless Apps (using Lambda)
> Data sets with simple access patterns

## Key Concepts
> Tables, Items and Attributes
- A table is a grouping of data records
- An item is a single data record in a table
- Attributes are pieces of data attached to a single item

> Primary Key
- Each item in a table is uniquely identified by a primary key
- defined at the creation of the table
- key must be provided when inserting a new item
- Two types of primary keys
1. simple primary key made up of just a partition key ( standard key-value stores)
2. composite primary key made up of a partition key and sort key ( sort items; Customer id)

*each item in a table is uniquely identified by a primary key, even with the composite key*

> Secondary Indexes
- secondary indexes to enable additional access patterns
- local secondary index: uses the same partition key but a different sort key 
- global secondary index: artition key for a table with a composite primary key (useful in getting the most out of DynamoDB)


# Redshift
## Resource
[REDSHIFT](https://www.tutorialspoint.com/amazon_web_services/amazon_web_services_redshift.htm)

> managed data warehouse service in cloud
> datasets: 100s of gigabytes to petabytes
> nodes: to create a data warehouse is to launch a set of compute resources
> nodes are organized into clusters to process queries

### Setup Redshift
1. Sign in & Launch REDSHIFT CLUSTER
2. Setup security group for client connection
3. Connect to Cluster

> Features: 
- Suppots VPC
- Encryption
- SSL
- Scalable
- Cost-effective

# Amazon DMS 
## DATA MIGRATION SERVICE
### Resource
[DMS](https://www.amazonaws.cn/en/dms/)
> Data migration with little down time and securily
> database remains fully operational during the migration
>  supports homogenous migrations 
> heterogeneous migrations is also supported (different databases)

### Benefits
- Simple
- Quick / Fast
- Suppots all databases
- Cheap
- one-time migration or on-going replication
- Reliable 

### Uses
1. Homogeneous Database Migrations
2. Heterogeneous Database Migrations
3. Development and Test
4. Database Consolidation
5. Continuous Data Replication










