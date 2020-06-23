# Defining what we mean by Migration
- Process of moving resources to a cloud environment
- Five phases:
    - Migration preparation adn business planning
    - Portfolio discovery and planning
    - Designing migrating and validating applications (4 , 5 )
    - Operate
# Migration Preparation and Business Planning (Phase 1)
- prepare a plan to minimize risk accordingly to the complexity of the architechture to migrate
# Portfolio Discovery and Planning (Phase 2)
- Where are dependencies between apps
- build use case and app case for each appplication
# Design, Migration and Application Validation (Phase 3 & 4)
- Design and act to migrate resources
- 6R:  Rehost, Replatform, Repurchase, Refactor, Retire, Retain
# Operate (Phase 5)
- Look for services candidates to be retired
- partners 
# Cloud Adoption Framework
- Build an approach to cloud from organization
- Business and people perspective, governance, technical perspective, security , operation
# Scaling Considerations
- Scaling constraints:
    - not every server can scale, use off-server session storage or other resources, remove unnecesary load from nos-scalable servers
- Horizontal scaling: add resources to add capability and distrubite load between
- Vertical scaling: make the resources more capable of responding to more requests
# High availability
- designing for the highest levels of uptime
- avoid single points of failure
- distribute traffic between various nodes
# Considerations with migrating DB vs applications
- Consider schema, model and engine changes
- Planning human resources for migration
- planning times
# AWS Server Migration Services
- only available for migrating VMware, vSphere, Microsoft Hyper V and Azure virtual machines
- Replicate server as AMIs available for deploying in EC2
- Set alarms with Cloudwatch and Cloudtrail
# VM import VM on AWS
- VM import: import machines from premises from AWS as EC2 images
- AWS server migration SMS automates the process of importing
# AWS migration hub
- chose the tools that best fit your needs
- see metrics and progress
# AWS application discovery
- 2 ways: agentless and agent based, identify info about servers
- utilization metrics to decide sizes from AWS services
- agent based: install aWs agent in every resource in premises
- integrated with migration hub
- create cost optimized migration plan








