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


![image](https://github.com/user-attachments/assets/62d21ee4-424d-4c0f-985d-7f975209fb04)


![image](https://github.com/user-attachments/assets/1da52070-cb7d-4aad-af6a-a62ae3a6eed6)


![image](https://github.com/user-attachments/assets/dd647a35-8501-4c02-a236-156fc103a06e)

![image](https://github.com/user-attachments/assets/2b0ca9c6-d1db-4d84-aae7-6dfd44a66935)


![image](https://github.com/user-attachments/assets/660a357a-7007-47f9-9b8c-18edabf3dd19)


![image](https://github.com/user-attachments/assets/c560b7ed-9817-4672-b5c9-d3a7b201979b)


![image](https://github.com/user-attachments/assets/c80f13e3-b2fb-4829-b448-cecf6b9e039c)


![image](https://github.com/user-attachments/assets/94aca0b8-dbf2-4a26-a827-893889568799)


![image](https://github.com/user-attachments/assets/99fe5c9f-9f54-48d2-a895-75f8e5323a52)




