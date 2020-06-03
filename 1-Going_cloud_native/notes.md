# AWS Overview Notes

Six Advantages and Benefits of Cloud Computing

- Trade capital expenses for variable expense
- Benefit from massive economies of scale
- Stop guessing capacity
- Increase speed and agility
- Stop spending money on running and maintaining data centers
- Go global in minutes

# AWS infrastructure

- region: geographically located resources (storage, compute, laws etc)
- availability zones: guarantee highly available services

# Compute services in AWS

## EC2
- elastic compute cloud: servers on demand
- AMI: amazon machine image
- tags: actegorize EC2 instance
- security group
- **EC2 Instance types:**
    - General purpose: balanced, use cases as web servers or code repositories A1, T3, T3a, T2, M6g, M5, M5a, M5n, M4
    - Compute optimized: for applications that benefit from high performance processors, HPC, gaming servers, ad server engines, machine learning inference C%, C5n, C4
    - memory optimized: apps that process large datasets in memory, high performance DB, big data analytics, R5, R5a, R5n, R4, X13, X1, high memory, Z1D
    - Accelerated Computing: use hardware accelerators, or co-processors, to perform functions, such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs. speech recognition, autonomous vehicles, P3 , P2, inF1, G4, G3, F1
    - Storage Optimized:  that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver tens of thousands of low-latency, random I/O operations per second, NoSQL DB, in-menmory DB, data warehousing I3, I3en, D2, H1
- Fixed ( eg M5, C5, R5) and burstable performance (T).
- **Lightsail:** offers environments eg. for wordpress sites, node servers, containers etc
# Networking and storage
## VPC
- Define a net where the applicatiosn run, we can define subnets.
- Define private IPs 10.10.0.0/16
- Define IGW (internet gateway) to communicate the vpc / VGW to access pricate subnets
- Create a route table add 0.0.0.0/0 (internet) and associate to the subnet
- Databases should go in private subnets
- We can create replicate subnets in other availability zone for high availability
- VPC are multi AZ structures
- ELB: elastic load balancer
- Classless Inter-Domain Routing: CIDR network addresses are allocated in a virtual private cloud (VPC) and in a subnet by using CIDR notation. A /16 block provides 65,536 IPv4 addresses. A /24 block provides 256 addresses.

# Storage
- S3: Object level storage
- RDS: Block storage 
## EBS
- EBS (elastic block storage) : define volumes to attach to EC2 machines
## S3
- simple storage service, object storage (images or text, media, backups)
- Buckets: have an url accesible over http or https, object private by default
- objects can be up to 5TB
- control permission over the bucket and select region to optimize
## Amazon Elastic File System (Amazon EFS)
- Regionally distributed, can attach to n EC2 instances simultaneously
# Databases
## RDS
- have a VPC and subnet created
- choose the DB engine (amazon aurora, postgres, mysql, mariadb, oracle, microsoft sql server)
- use case: production(multi AZ) or dev/test
- AWS DMS migration service
## Dynamo DB
- Create a table
- single-digit millisecond latency at any scale
- document and key-value storage models
# Monitoring applications
## cloudwatch
- Collect and track metrics, collect and monitor log files, set alarms, and automatically react to changes in your AWS resources.
- Events: set rules, respond to changes in aws resources and route the to functions
- Logs metrics: collect logs metric by installing cloudwatch agent on the server
## load balancing
- ELB: regional in the VPC, automatic trafic to the instances
    - application lb: request level (layer 7) routing trafic to EC" instances, microservices and containers, based on content of request, ideal fot HTTP/HTTPS traffic advanced lb
    - Network LB: layer 4, connection level, routes based on IP protocol data, ideal for TCP traffic
    -  Classic LB: basic lb across ec2 instances, request and connection level
## Auto scaling
- Create an auto scaling group
    - configure AMI and configuration 
    - configure scaling policies with cloudwatch metrics
# Security and Cost Management
## Security
- Hypervisor, network, and physical layers are AWS responsibility, things as Guest OS, Application and User Data is user responsibility on EC2
- RDS, user only have to worry about user data
## Cost management
- AWS cost explorer: reports
- AWS budgets: alerts and threesholds for cost
- AWS trusted advisor: tool to identify areas to optimize (cost, performance, security, fault tolerance, service limits) 








