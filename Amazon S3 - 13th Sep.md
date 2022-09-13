# Amazon S3
### Resource
(https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

**Amazon Simple Storage Service is a storage service**
> Scalability
> Data Availability
> Security
> Performance

*Can be used to store and protect data for data lakes, websites, apps, backup etc* 


## Features
1. Storage classes
- store mission-critical production data (frequent access)
- store infrequently accessed data in S3 Standard-IA (saves cost)
- Archive data at low cost
- optimizes storage cost by automatically moving data between the four teirs
- These four access tiers include two low-latency access tiers optimized for frequent and infrequent access
- Different storage classes for different uses

2. Storage management
- used to manage costs
- meet regulatory requirements
- reduce latency
- save multiple copies 
- S3 Lifecycle: policy to manage and store objects at low cost, objects can be transistioned
- S3 Object Lock: Prevents objects from being deleted, WORM storage, adds a layer of protection
- S3 Replication: Replicates data for different regions or buckets
- S3 Batch Operations: You can use Batch Operations to perform operations such as Copy, Invoke AWS Lambda function, and Restore on objects

3. Access management
- Features for auditing and managing access for buckets and objects
- S3 Block Public Access:  Block public access to S3 buckets and objects
- IAM: Create IAM users for your AWS account to manage access
- Amazon S3 accesss points:  Configure named network endpoints with dedicated access policies
- ACLs: Read and Write permissions for buckets and objects (Access Control Mechanism)

4. Data processing
- data and trigger workflows to automate a variety of other processing activities
- Features: S3 Object Lambda, Event notifications

5. Storage logging and monitoring
- used to monitor and control how your Amazon S3 resources are being used
- Automated Monitoring Tools: Amazon CloudWatch metrics (Health of resources), AWS CloudTrail (Records actions)
- Manual Monitoring Tools: Server access logging (detailed records for requests), AWS Trusted Advisor (Evaluation using best practice checks)

6. Strong Consistency
-  read-after-write consistency for PUT and DELETE requests


## Amazon S3 working
> it is basically a object storage service, data is stored in the form of objects in buckets
> A bucket is a container for objects

1. First create a bucket (with name and region)
2. Upload data as objects (objects have specific key)
3. Buckets and objects are private (only accessed if permission)


## Amazon S3 data consistency model
Amazon S3 achieves high availability by replicating data across multiple servers within AWS data centers,
- process writes a new object to Amazon S3 and immediately lists keys within its bucket. The new object appears in the list
-  process replaces an existing object and immediately tries to read it. Amazon S3 returns the new data
- A process deletes an existing object and immediately tries to read it, no data is returned if object is deleted
- A process deletes an existing object and immediately lists keys within its bucket, not in listing

# Accessing S3
1. AWS Management Console: web-based interface
2. AWS Command Line: issues commands
3. AWS SDKs: consists of libraries and sample code (convenient way to create programmatic access)
4. Amazon S3 REST API: programming language-neutral (The REST API is an HTTP interface)

Note: PCI DSS compliance 
supports the processing, storage, and transmission of credit card data by a merchant or service provider, and has been validated as being compliant with Payment Card Industry (PCI) Data Security Standard (DSS)

