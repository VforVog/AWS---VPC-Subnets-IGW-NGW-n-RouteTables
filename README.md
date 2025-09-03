## 📖 Project Overview

This project demonstrates the **architecture and hands-on implementation of AWS networking fundamentals** using best practices.  

The setup includes:  
- A **custom VPC** with public and private subnets  
- An **Internet Gateway** for public resources  
- A **NAT Gateway** for secure outbound access from private resources  
- **Route Tables** configured for proper traffic routing  
- **EC2 instances** deployed in both subnets to test connectivity and isolation  

The public EC2 (bastion host) acts as a secure entry point, while the private EC2 is isolated from the internet and only reachable internally. ICMP (ping) and SSH were used to validate connectivity.  

<br>

## 🛠️ Technologies Used

> 📦 **Infrastructure Components**
> - Amazon VPC (CIDR: 10.0.0.0/16)  
> - Public Subnet (10.0.1.0/24)  
> - Private Subnet (10.0.2.0/24)  
> - Internet Gateway (IGW)  
> - NAT Gateway with Elastic IP  
>
> 💻 **Compute**
> - EC2 Instance (Public) → Bastion Host with Public IP  
> - EC2 Instance (Private) → Backend/Database server (no Public IP)  
>
> 🔒 **Security**
> - Security Groups (SSH, ICMP for testing)  
> - Route Tables (Public → IGW, Private → NAT)  
>
> ⚙️ **Tools**
> - AWS CLI (via Git Bash / VS Code terminal)  
> - Key Pairs (.pem) for SSH Access  



## 🛠️ Technologies Used

| Service            | Purpose                                                                 |
|--------------------|-------------------------------------------------------------------------|
| **🏗️ Infrastructure** | *Core networking resources*                                           |
| 📦 **Amazon VPC**     | Custom virtual network (CIDR 10.0.0.0/16) to isolate resources.          |
| **Subnets**        | Public (10.0.1.0/24) for bastion host, Private (10.0.2.0/24) for backend.|
| **Internet Gateway** | Enables internet access for resources in the public subnet.            |
| **NAT Gateway**    | Allows private subnet instances to initiate outbound internet traffic securely. |
| **Route Tables**   | Control traffic flow: Public → IGW, Private → NAT Gateway.               |
| **Key Pairs **   | Public and Private key files(.pem) for SSH Access                 |
| 💻 **EC2 Instances**  | Public EC2 (bastion host with SSH + public IP) and Private EC2 (no public IP). |
| 🔒 **Security Groups**| Control inbound/outbound rules (SSH, ICMP for testing).                  |
| **Elastic IP**     | Provides a stable IP for the NAT Gateway.                               |
| ⚙️ **AWS CLI**        | Used for configuration and SSH connectivity testing via Git Bash/VS Code. |



# <p><b>Architecture</b></p>

<br>

![Image Description](Picture1.jpg)

<br>
<br>

# <p align="center"><b>Simulation</b></p>

<br>

![Lex Demo](gif/gif.gif)

