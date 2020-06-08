# Shared Responsibility
## AWS responsibility “Security of the Cloud” 
- harware, software, network and infrastructure that runs AWS services
## Customer responsibility “Security in the Cloud”
- perform the necesary security configuration in each of the services
## Compliance
- understand compliance objectives and requirements
- establish controlled environments that meet objectives and reqs
- understand validation required based on the organization risk tolerance
- verification of operating effectiveness of controlled environment
# Create an Account
- Create users and set permissions, don't use the root account
- MFA multi factor authentication: ask for a code from app or device
- IAM (identity and access management) 
## Multiple accounts
- IAM group: create group, add policies
- Users: create with username and access type (programatic with key and secret and aws management console), add user to a group, create tags, download the access key and secret info
- **AWS Organizations:**
    - Automate account creation
    - Create groups of accounts
    - Govern access to AWS services resources region by policies
    - Set up payment for all accounts with consolidated billing
    - Share resources across acounts
- plan structure, keep master account free of operational resources, AWS cloudtrail, Least privilege practice, assign policies to roganizational units, test new and modified policies, use APIs
# Identity and access services
- Use cases:
    - Members logging into AWS
    - Applications using Resources (ej service using RDS database)
    - Users login to application
- AWS Organizations: group accounts
- IAM: identity and acces management: manage users, roles, federated users. Use any identity management solution that supports SAML 2.0 or AWS federation samples (AWS Console SSO or API Federation) IAM policy simulator to test permissions
- AWS single sign on SSO
- Amazon Cloud Directory: establish directories with different hierarchies in multiple dimensions.
 # Directory services
 - Amazon cognito: user portal to manage users
 # Network isolation VPC
 - Public subnets can connect to internet (NACLs)
 - Security groups act as firewalls for EC" instances controlling traffic at instance level
 # VPC endpoints and private links
 - private link: traffic between AWS but not through the internet
 - route tables: set of rules, where network traffic is directed
 - Each subment must be associated to a route table, only one, but a route table can have n subnets 
 - **AWS Direct Connect:** service to connect on-premise resources to AWS, establish a dedicated network connection between user network and aws
 # Detective Controls
 -  auditing, automated analysis, and alarming
 # Auditing: 
 - AWS Cloudtrail: who is doing what
 - AWS config: record configurations and changes to it
 - Amazon inspector: automated security assesments:
    - Network configuration reachability
    - Amazon agent
    - Security assessment service
- AWS trusted advisor: report with recomendations
# Monitoring CloudWatch and CloudWatch logs
- Retrieve metrics from resources, set alarms, logs
# Monitoring Guard Duty and Security Hub
- GuardDuty: threat detection srvice that monitor for malicious or unauthorized behaviors
    - low, medium and high severity levels
    - HTTPS APIs, cloudwatch events: trigger events and functions to respond 
- AWS Security Hub: centralize AWS GD, A. Inspector, Amazon Macie and AWS Partner Solutions


