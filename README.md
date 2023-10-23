# 3_Tier_Web_Architecture_AquilaCMS

- This Architecture is not focusing on Availability and Scalability .

# Structure 

  1. Web/Presentation Tier: Houses the user-facing elements of the application, such as web servers and the interface/frontend.
  2. Application Tier: Houses the backend and application source code needed to process data and run functions.
  3. Data Tier: Houses and manages the application data. Often where the databases are stored.
    
  - Each tier has its own security group that only allows the inbound/outbound traffic needed to perform specific tasks.
  - The underlying network architecture
    1. A VPC.
    2. public subnet ( Web Tier)
    3. private subnet (Application Tier).
    4. private subnet (Database Tier). We are using Mongodb in EC2
    5. public route table that connects the public subnet to an internet gateway.
    6. private route table that will connect the Application Tier private subnet and a NAT gateway.

  - Services Used
    1. VPC
    2. NAT gateway
    3. subnets
    4. EC2
    5. EC2(For MongoDB)
    6. IAM
   
# Setting up Aquilla 

1. To install the latest AquilaCMS, you need :
  - node.js 18.16.0+ (tested in v14.20.1+ and v16.18.1+)
  - mongoDB 6.0.2+ (tested in v4.2.5+) // for AWS we are EC2 instance with mongoDB installed
  - yarn 3.4.1+ package manager (tested in v1.22.19 and v4.0.0-rc.35)

For further details check -> https://github.com/AquilaCMS/AquilaCMS

