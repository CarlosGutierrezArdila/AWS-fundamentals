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

