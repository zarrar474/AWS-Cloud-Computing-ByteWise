# Shared Responsibility Model
### Resource
[Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)

- help relieve the customer’s operational burden
- AWS operates, manages and controls the components from the host operating system and virtualization layer down to the physical security
- Guest OS, updates and security patches
- provides the flexibility and customer control that permits the deployment
- Security “of” the Cloud versus Security “in” the Cloud.

## Security of the Cloud AWS RESPONSIBILITY
> protecting the infrastructure that runs all of the services offered in the AWS Cloud (hardware, software, networking, and facilities)

### Security in the Cloud CUSTOMER RESPONSIBILTY
> the amount of configuration work the customer must perform as part of their security responsibilities
> shared responsibility model also extends to IT controls
> relieve customer burden of operating controls by managing those controls associated with the physical infrastructure

*Inherited Controls – Controls which a customer fully inherits from AWS.*
*Shared Controls – Controls which apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives. In a shared control, AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services.*

- Patch Management (correcting flaws and loopholes)
- Configuration Management (customer is responsible for configuring the guests OS)
- Awareness & Training (Customer has to train their own employees)

*Customer Specific – Controls which are solely the responsibility of the customer based on the application they are deploying within AWS services*
- Service and Communications Protection or Zone Security
