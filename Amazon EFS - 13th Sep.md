# Amazon Elastic File System

## Resource 
(https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html)

*Amazon EFS is a simple and serverless elastic file system*

- Built to scale on demand without disruptions and with automatic shrinking due to files
- no provison or management of capacity for growth
- simple interface to create files quickly 
- manages all the file storage infrastructure for you
- Only pay for storage used by your files 
- no minimum fee or setup cost

## Storage Classes

> Standard Storage Classes: resilience and the highest levels of durability and availability
> One Zone Storage Classes:  offer customers the choice of additional savings by choosing to save their data in a single Availability Zone

-  General Purpose performance mode is ideal for latency-sensitive use
- can scale to higher levels throughput and operations per second with a tradeoff of higher latencies for file system operations
- Throughput mode: scales as your file system grows.
- Provisioned Throughput mode:  can specify the throughput of your file system independent of the amount of data stored

*designed to be highly scalable, highly available, and highly durable*
EFS has strong data consistency and file locking
> you can control access to your file systems via Portable Operating System Interface

- Authentication
- Authorization
- Encryption

