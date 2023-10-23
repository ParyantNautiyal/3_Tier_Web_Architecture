# 3_Tier_Web_Architecture

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
    4. private subnet (Database Tier).
    5. public route table that connects the public subnet to an internet gateway.
    6. private route table that will connect the Application Tier private subnet and a NAT gateway.

  - Services Used
    1. VPC
    2. NAT gateway
    3. subnets
    4. EC2
    5. RDS
    6. IAM
