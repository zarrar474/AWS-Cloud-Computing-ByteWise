# Amazon Elastic Block Store (Amazon EBS)

 > Amazon EC2 instance type come with directly attached storage devices (instance store)
 > Instance stores are good for temporary storage
 > Since data stored can be terminated or instances can stop
 > For long term storage of data use Amazon EBS
 > Best Practise: Perform Regular Snapshots and AWS Backup
 
## DeleteOnTermination: instance's root volume is set to true, root volume is deleted when instance terminates
 > DeleteOnTerminarion attribute can be set to false
 
Note: The size of an instance store as well as the number of devices available varies
