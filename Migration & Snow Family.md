# 6 Ways to Migrate Apps to Cloud
### Resource 
[Migration Strategies](https://aws.amazon.com/blogs/enterprise-strategy/6-strategies-for-migrating-applications-to-the-cloud/)

## Creating a Migration Strategy
*what’s in their environment, what are the interdependencies, what’s going to be easy to migrate and what’s going to be hard to migrate, and how they’ll migrate each application*
- Outline a plan (subject to change)
- order of migrating each app
- difficulty of migrating apps depends on the apps itself (architecture, licensing arrangement)
- service-oriented architecture ; low-complexity
- monolithic mainframe ; high-complexity 
- start with less complex apps

## The 6 R's
*6 common strategies*

1. Rehosting (lift and shift):
- new development using cloud-native capabilities
- saves cost, quick migration, requirments is to scale quickly
- rehosting can be automated or manually 
2. Replatforming (lift tinker and shift)
- need to make cloud optimizations for benefits
- core architecture remains the same
- Elastic Beanstalk or RDS (management) 
3. Repurchasing (different product)
- repurchasing as a move to a SaaS platform
4. Refactoring / Re-architecting (changing architecture and development of app)
- use cloud native features
- need to add features, scale and performance (difficult on current enviornment)
- most expensive
5. Retire (get rid of it)
- not useful features need to be turned off
- savings
- lessen surface area
6. Retain (revisit) 
- only migrate some useful applications
- cost effective
- gradually move from on-premises to cloud

# AWS SNOW FAMILY
*MOVING DATA TO AND FROM AWS*

- Devices to move data cost effectively (OFFLINE)
- Snow devices move data
- High Security
- compute and storage compatible
- different devices depending on  space and weight and portability options

## KEY FEATURES: 
1. Simple management and monitoring (GUI Available)
2. On-board computing
3. Encryption (256-bit encryption key : AWS KMS)
4. End to end tracking (E-Ink shipping label)
5. Secure erasure (after migrations, aws performs a software erasure)
6. NFS endpoint 
7. Anti-tamper & Tamper-evident ( Trusted Platform Module (TPM) )

## Service models of snow family
1. Snowcone: most compact and portable device
2. Snowball: Compute Optimized device or a Storage Optimized device
3. Snowmobile: Exabyte-scale data migration device for **large amounts of data**
