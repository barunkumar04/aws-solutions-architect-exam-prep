## Getting started

- Amazon started AWS in 2002. First offering was SQS.
- AWS Global Infrastructure are
  - AWS Regions
  - AWS Availibility Zones
  - AWS Data Centers
  - AWS Edge Locations / Points of presence

- How to choose a AWS region?: It depends, but there are few factor which can help choosing
  - Complaince: Sometimes governments want the data to be local to the country you're deploying the application in. For example, France, data in France may     have to stay in France and therefore you should launch your application in the French region.
  - Proximity to users/customer: Data near to user, reduces latency.
  - Available services in region - Not all region has all services.
  - Pricing: Pricing varies region to region.

- Region / Avaailablity Zone / Data Center - What stands where?
 <img width="700" alt="image" align = "center" src="https://user-images.githubusercontent.com/22455492/178155498-34545b34-8908-4a7a-986d-4790308590b6.png">


## IAM (Identity and Access Management) and AWS CLI

- IAM is a Global Service
- IAM Policy structure: IT consists of
  - Version
  - Id
  - Statment(s)
  - And, Condiiton: This is optional and represnet condition on this policy is applied or not
    ![image](https://user-images.githubusercontent.com/22455492/178217419-ddadf419-05d7-4329-983f-528dd5dca89d.png)
    
### Securing IAM (User/Groups) 
  - Setup password policy
  - Setup MFA (Multifactor Factor Authentication)
    - MFA = Password you know + Security Device you know
    
### Ways to access AWS Account and How are they protected
  - AWS Management console: Protected by password + MFA
  - AWS CLI: Protected: Protected by access key,Access key is created using AWS Console, unser User section.
  - AWS CloudShell: An alternative to CLI. Not available in all regions
  - AWS Software Developer Kit (SDK): For code, protected by access key

### [REVISIT] IAM Role for services
  - Sometime AWS services like EC2, lamda access our account. To let that happen, we need to created role and assign to our services. For example - EC2 Instance Roles, Lambda Functions Roles.

### IAM Best Practices
  - Do not use a root accounts except when you set up your AWS account.
  - Assign users to groups and assign permission to groups to make sure.
  - Create a strong password policy and if possible use MFA.
  - Use access keys for programetcally access of AWS account
  - Audit permissions within your accounts, you can use the IAM Credentials Reports, and also IAM access analyzer.

### IAM Summary
  - Users: mapped to a physical user, has a password for AWS Console
  - Groups: contains users only
  - Policies: JSON document that outline permissions for users or groups
  - Roles: For EC2 instance or AWS Service
  - Security: MFA + Password Policy
  - Access Key: access AWS using AWS CLI or SDK
  - Audit: IAM Credential Report & IAM Access Advisor 


## EC2 Fundamentals

### AWS Budget setup 
  - By default IAM user doesn't has permission to setup a AWS Budget. 
  - Root user must provide the permission to IAM user, if an IAM wants to setup a AWS Budget. Follow Login using Root user -> Account -> Activate from here
  - Budget is setup on account level. There are multiple kind of budget which can be setup, Cost budget is recomended one. 
  - Using budget we can set setup level wise alerting. For example, first alert on 80% of budget amount consumption and so on.
  - There is also a provision to define action upon reaching the alert. This is optional.
