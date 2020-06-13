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
 - Security groups act as firewalls for EC2 instances controlling traffic at instance level
 # VPC endpoints and private links
 - private link: traffic between AWS but not through the internet
 - route tables: set of rules, where network traffic is directed
 - Each subnet must be associated to a route table, only one, but a route table can have n subnets 
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
# Data types
- prevent accidential CRUD
- **Data type       |   AWS service**
- Object:               S3 /S3 glacier
- Database:             RDS, timestream, Quantum ledger database, neptune
- EC2 data:             EBS, EFS
- Data warehouse:       Redshift, Athena
- Data lake:            Lake formation
- Data transfer:        Snowball, Snowmobile

- Amazon aurora MySQL 5x more performant, Postgres 3x more performant
# Encryption in transit
- define requirements for data protection in transit
- Apply encryption
- Authenticate network communication
- IPSec: protect data on layer 3
- TLS ans SSL 
- ACM aws certificate manager 
# Encryption at rest
- KMS: key manage service
- CMK customer master keys
- cloudHSM hardware security management
# Database Encryption
- inside VPC: load balancer and web server in public subnet, internal load balancer and app server in private subnet
- RDS: underlying storage is encrypted, as are its automated backups, read replicas, and snapshots.
- SSL for data in transit
- Encrypt with AES256 when creating RDS instance, KMS used to manage encryption key
- DynamoDB is encrypted by default
# Amazon s3
- Bucket policies IAM policy
- Enable default encryption
- server side encryption with Amazon S3 managed SSE-S3 or KMS-managed SSE-KMS
- Macie uses machine learning to discover sensitive data to encrypt
- When you use server-side encryption, Amazon S3 encrypts an object before saving it to disk and decrypts it when you download the objects
# EBS encryption
- set encryption by default for new EBS volumes and snapshots
# Protecting Compute Resources
## EC2
- User: Operating System / Identity management system that provides access
- AWS: Hypervisor / EC2 instance isolation
- Restrict access at Network and OS level
- Control API access with IAM roles
## Containers
- Docker: AWS elastic container service ECS, elastic kubernetes service EKS, Fargate, Elastic Beanstalk
## AWS Lambda
- AWS: infrastructure, OS, App platform
- User: security of the code
- Storage and accesibility of sensitive data
- IAM to lambda service withn function
# Securing Endpoints
- Application loas balancer (single requests) layer 7
- Network Load Balancer layer 4
- API Gateway: expose REST or other services
    - AWS Signature Version 4 (sigV4)
    - Lambda authorizor (JWT, OAUTH)
# Securing secrets
- AWS Secrets Manager: handle access to secrets without storing on any instance, server or container
# Well architected tool
pilars:
- Security
- Reliability
- Performance efficiency
- Cost Optimization
- Operational Excellence











