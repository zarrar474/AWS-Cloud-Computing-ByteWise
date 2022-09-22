# Global Networking in AWS 

### Resource: [Network ACLs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html)

## Network Access Control List (ACL)
- ACL is a network at allows or denies, incoming and outgoing traffic (at subnet level)
- Can create a custom network ACL for additional secuirty 

Network ACL A determines which traffic destined for subnet 1 is allowed to enter subnet 1, and which traffic destined for a location outside subnet 1 is allowed to leave subnet 1. Similarly, network ACL B determines which traffic is allowed to enter and leave subnet 2.


![Network ACL](https://github.com/zarrar474/AWS-Cloud-Computing-ByteWise/blob/main/network-acl.png)

## ACL Basics
1. VPC comes with a defualt ACL which can be modified 
2. You can create custom ACL and add to subnets (rules need to be added)
3. Every subnet must be associated to a ACL (when associated, previous ACL is removed)
4. Network ACL has inbound rules and outbound rules (to allow or deny traffic), rules have number 1 to 32766
5. Create rules in increments, so that new rules can be inserted afterwards
6. Evaluate the network ACL rules when traffic enters and leaves the subnet, not as it is routed within a subnet
7. Network ACLs are stateless
8. Quotas/ Limit for number of ACLS per VPC  **Amazon Virtual Private Cloud (Amazon VPC)**

## ACL Rules
- Rule Number:  evaluated starting with the lowest numbered rule
- Type: Type of traffic (specify all traffic or a rang eof traffic)
- Protocol: can specify any protocol that has a standard protocol number
- Port Range: The listening port or port range for the traffic
- Source:  The source of the traffic (for inbound traffic only)
- Destination: Destination of traffic (for outbound traffic only)
- Allow/ Deny: Whether to allow or deny the specified traffic

*If you add a rule using a command line tool or the Amazon EC2 API, the CIDR range is automatically modified to its canonical form*


## Defualt ACL 
- Configured to allow all traffic to flow in and out of the associated subnets
- Each network ACL also includes a rule whose rule number is an asterisk
- The asterisk rule applies if a packet doesn't match any rule
- This * rule can't be modified or removed

*Note
If you've modified your default network ACL's inbound rules, we do not automatically add an allow rule for inbound IPv6 traffic when you associate an IPv6 block with your VPC. Similarly, if you've modified the outbound rules, we do not automatically add an allow rule for outbound IPv6 traffic.*


## Custom ACL 
- You might want to add a *deny rule* in a situation where you legitimately need to open a wide range of ports, but there are certain ports within the range that you want to deny
- You can also add 8allow rules* depending on the use case
- make sure there is a corresponding inbound and outbound rule for the rules you add

## Ephemeral Ports (Range of 32768-65535)
-  use a different range for your network ACLs depending on the type of client

## Path MTU Discovery {maximum transmission unit (MTU)}
- Used to determine the path MTU between two devices.
- path MTU is the maximum packet size that's supported on the path Between 2 hosts

**Important:
Be very careful if you are adding and deleting rules at the same time. Network ACL rules define which types of network traffic can enter or exit your VPCs. If you delete inbound or outbound rules and then add more new entries than are allowed in Amazon VPC quotas, the entries selected for deletion will be removed and new entries will not be added**









