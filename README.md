# 🌐 AWS CloudFormation Modular Infrastructure

This project defines a complete AWS infrastructure using **nested CloudFormation stacks** to promote reusability, modularity, and clean architecture practices.

## 🏗️ Architecture Overview

- **VPC Stack** – Creates a VPC, public/private subnets, and Internet Gateway.
- **S3 Stack** – Creates a versioned, private S3 bucket for environment-specific storage.
- **Compute Stack** – Sets up ALB, EC2 instances, Auto Scaling, and security groups.
- **RDS Stack** – Provisions a MySQL RDS instance with private subnet group and secure credentials.
- **Root Stack** – Orchestrates all above stacks with parameter passing and output consolidation.

## ⚙️ Technologies Used

- AWS CloudFormation (YAML)
- EC2 + ALB + ASG
- Amazon RDS (MySQL 8.0.40)
- Amazon S3
- Amazon VPC


## 🔐 Security Highlights

- `NoEcho` used for sensitive parameters like DB passwords
- Strict CIDR blocks for RDS and EC2 security groups
- S3 bucket name uniqueness with `AccountId`
- Public access is disabled where not necessary

## 📁 Folder Structure
. ├── rootstack.yaml ├── vpcstack.yaml ├── compute.yaml ├── rdsstack.yaml └── s3bucket.yaml 


Upload all templates to S3 and deploy the `rootstack.yaml` via the console or CLI. Provide required parameters like `DBPassword`, `KeyName`, etc.

> 💡 Ensure DB password does not contain invalid characters like `/`, `@`, `"`, or spaces.



## Output Screenshots


![image](https://github.com/user-attachments/assets/d90a8907-a8cd-4a89-aae2-a95b8c8cf140)



![image](https://github.com/user-attachments/assets/b1f3a1d7-d4b7-495a-bfb5-6f9a55613e39)



![image](https://github.com/user-attachments/assets/1d520742-0474-41b4-b13e-aabebe44da29)




![image](https://github.com/user-attachments/assets/2630099b-782a-4739-9e39-c2aa774fc03b)




![image](https://github.com/user-attachments/assets/5c474807-01c3-4d51-aa1b-608415101153)




![image](https://github.com/user-attachments/assets/c2c2b57f-d6ce-4347-ad74-852010d1fe28)




![image](https://github.com/user-attachments/assets/0cd3ad9d-91de-40c6-b10a-604fce6ceb2a)



![image](https://github.com/user-attachments/assets/a4727aac-2219-4a86-8588-2df15c2238db)





![image](https://github.com/user-attachments/assets/dc01d82b-22f0-45b0-b601-361767e45ed3)




![image](https://github.com/user-attachments/assets/3a238a96-b3c7-49f7-a7df-88065b33050c)





![image](https://github.com/user-attachments/assets/015b3feb-3d02-418c-93c6-c6dc33f8d500)

