# VPC - Virtual Private Cloud
## What is VPC
    A Virtual Private Cloud (VPC) is a logically isolated section of the AWS Cloud where you can launch AWS resources (like EC2 instances, RDS databases, Lambda functions, etc.) in a virtual network that you define. It provides control over your networking environment, including:
        IP address ranges
        Subnets
        Route tables
        Security groups & NACLs (Network Access Control Lists)
        Internet gateways & NAT gateways
        VPN & Direct Connect connections
### Default VPC on AWS
![alt text](<images/Default VPC on AWS.png>)

### CIDR - Subnet Mask
![alt text](<images/CIDR-Subnet Mask.png>)

### Public vs Private IP
![alt text](<images/Public vs Private IP.png>)

## Key Components of a VPC
    Subnets
    Route Tables
    Internet Gateway (IGW)
    NAT Gateway / NAT Instance
    Security Groups & NACLs
    VPC Peering
    VPC Endpoints

![alt text](<images/VPC Components.png>)

## VPC in AWS - IPv4
![alt text](<images/VPC in AWS - IPv4.png>)

### Create VPC
![alt text](<images/Creating a VPC.png>)

### Created VPC in AWS
![alt text](<images/Created VPC.png>)

## VPC - Subnet (IPv4)
![alt text](<images/VPC - Subnet (IPv4).png>)

### Adding Subnet
![alt text](<images/Adding Subnets.png>)

### Adding Subnet on AWS
    CIDR calculation: https://www.ipaddressguide.com/cidr
![alt text](<images/Adding Subnet on AWS.png>)

## Internet Gateway (IGW)
![alt text](<images/Internet gatway (IGW).png>)

### Adding Internet Gateway
![alt text](<images/Adding Internet Gateway.png>)

### Adding Internet Gateway on AWS
![alt text](<images/Adding Internet Gateway on AWS.png>)

### Editing Route Tables
![alt text](<images/Editing Route Tables.png>)

### Editing Routes on AWS
![alt text](<images/Edit Routes on AWS.png>)

### Subnet associations
![alt text](<images/Subnet assiciation on AWS.png>)

### Create an EC2 instance using public subnet
![alt text](<images/Public EC2 Server.png>)

### Check the connection is this is working
![alt text](<images/SSH to EC2.png>)

## Bastion Hosts
![alt text](<images/Bastion Hosts.png>)

### Bastion Hosts on AWS
    - Create Bation Host server in Public subnet
![alt text](<images/Bastion Host on AWS.png>)

### Create Private EC2 instance in Private Subnet
![alt text](<images/Private EC2 server.png>)

### Establish connection from Bastion server to Private server
    - User the private key of the private sever that was created while using SSH
![alt text](<images/Bastion to Private subnet EC2 .png>)

## NAT Gateway (Network Address Tranformation)
![alt text](<images/NAT Gateway.png>)

### Adding NAT Gateway
![alt text](<images/Adding NAT Gateway.png>)

### Adding NAT Gateway on AWS
![alt text](<images/Adding Internet Gateway on AWS.png>)

### Adding Route for NAT
![alt text](<images/Adding Route to the NAT.png>)

### Check if the connection established between outside world and Private Server
![alt text](<images/NAT Established Connection to Private Server.png>)

### NAT with HA
![alt text](<images/NAT Gateway with High Availability.png>)

### NAT Gateway vs NAT Instance
![alt text](<images/NAT Gateway vs NAT Instance.png>)

### Security Groups & NACLs
    - NACLs (Netwok Access Control Lists) are stateless
    - Security Groups are stateful
![alt text](<images/Security Groups and NACLs.png>)

### NACL - Network Access Control List
![alt text](<images/Network Access Control List (NACL).png>)

### Adding NACLs
![alt text](<images/Adding NACLs.png>)

### Default NACL
![alt text](<images/Default NACL.png>)

### Ephemeral Ports
![alt text](<images/Ephemeral Ports.png>)

### NACL with Ephemeral Ports
![alt text](<images/NACL with Ephemeral Ports.png>)

### Create NACL rules for each target subnets CIDR
![alt text](<images/NACL rules for subnets CIDR.png>)

### Security Groups vs NACLs
    - Security Groups   # Stateful - Firewall for EC2 Instance
    - NACLs             # Stateless - Firewall for Subnets
![alt text](<images/Security Groups vs NACLs.png>)

### Adding NACL without rules on AWS
![alt text](<images/Adding NACL with out rules on AWS.png>)

### NACL connection denied by default
![alt text](<images/NACL Connection Denied.png>)

### Adding inboud and outboud rules in NACL
![alt text](<images/NACL adding inbound rules.png>)
![alt text](<images/NACL adding outbound rules.png>)

### NACL connection established after adding inbound and outboud rules
![alt text](<images/Connection Established after adding NACL Rules.png>)

## VPC Peering
    - Establish connectio betweein two VPC
    - CIDR can not be overlapped
![alt text](<images/VPC Peering.png>)

### VPC Peering - Good to know
![alt text](<images/VPC Peering - Good to know.png>)

### Adding VPC Peering
![alt text](<images/Adding VPC Peering.png>)

### Adding VPC Peering on AWS
![alt text](<images/Adding VPC Peering Connection on AWS.png>)

## VPC Endpoints (AWS PrivateLink)
![alt text](<images/VPC Endpoints (AWS PrivateLink).png>)

### Types of Endpoints
![alt text](<images/Types of Endpoints.png>)

### Gateway or interface Endpoint for S3
![alt text](<images/Gateway or interface Endpoint for S3.png>)

### Lambda in VPC accessing DynamoDB
![alt text](<images/Lambda in VPC accessing DynamoDB.png>)

## VPC Flow Logs
![alt text](<images/VPC Flow Logs.png>)

### Adding VPC Flow Logs
![alt text](<images/Adding VPC Flow Logs.png>)

### VPC Flow Log Syntax
![alt text](<images/VPC Flow Logs Syntax.png>)

### VPC Flow Logs - Troubleshoot SG & NACL issues
![alt text](<images/Troubleshoot SG and NACL issues.png>)

### VPC - Flow Logs - Architectures
![alt text](<images/VPC Flow logs - Architectures.png>)

### AWS Site-to-Site VPN
![alt text](<images/AWS Site-to-Site VPN.png>)

### Direct Connect (DX)
![alt text](<images/Direct Connect (DX).png>)

### Direct Connect - Connection Types
![alt text](<images/Direct Connect - Connection Types.png>)

### Site to Site VPN as a backup
![alt text](<images/Site to Site VPN as a Backup.png>)