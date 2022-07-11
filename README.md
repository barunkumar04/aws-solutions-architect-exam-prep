# Notes

### Getting started

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
 <img width="500" alt="image" align = "center" src="https://user-images.githubusercontent.com/22455492/178155498-34545b34-8908-4a7a-986d-4790308590b6.png">


### IAM (Identity and Access Management) AND AWS CLI

- IAM is a Global Service
- IAM Policy structure: IT consists of
  - Version
  - Id
  - Statment(s)
    ![image](https://user-images.githubusercontent.com/22455492/178217419-ddadf419-05d7-4329-983f-528dd5dca89d.png)
    
