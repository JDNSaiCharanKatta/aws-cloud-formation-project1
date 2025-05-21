# 🌐 AWS CloudFormation Modular Infrastructure

This project defines a complete AWS infrastructure using **nested CloudFormation stacks** to promote reusability, modularity, and clean architecture practices.


## ⚙️ Technologies Used

- AWS CloudFormation (YAML)
- EC2 + ALB + ASG
- Amazon RDS (MySQL 8.0.40)
- Amazon S3
- Amazon VPC


## 📌 Architecture Diagram

![image](https://github.com/user-attachments/assets/754de7a7-f9bd-4185-8431-8bf06cafa11a)



## 📁 Folder Structure
. ├── rootstack.yaml ├── vpcstack.yaml ├── compute.yaml ├── rdsstack.yaml └── s3bucket.yaml 


## ⚡ Deployment Steps  

Upload all YAML templates to an S3 bucket.  
Deploy rootstack.yaml via AWS Console or CLI.  
Provide required parameters like:  
  KeyName for EC2 access  
  DBPassword (restricted characters for security)  
The root stack orchestrates nested stacks automatically.  
Monitor stack outputs such as ALB DNS, RDS endpoint, and S3 bucket name.  






## 🔐 Security Highlights

- `NoEcho` used for sensitive parameters like DB passwords
- Strict CIDR blocks for RDS and EC2 security groups
- S3 bucket name uniqueness with `AccountId`
- Public access is disabled where not necessary



## Note 

Upload all templates to S3 and deploy the `rootstack.yaml` via the console or CLI. Provide required parameters like `DBPassword`, `KeyName`, etc.

> 💡 Ensure DB password does not contain invalid characters like `/`, `@`, `"`, or spaces.



## 📸 Screenshot Outputs


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

## ✅ What I Learned  
- CloudFormation Nested Stacks – Improved infrastructure organization and automated deployments.  
- Security Measures – Applied best practices to secure AWS services and minimize attack surfaces.  
- Auto Scaling & Load Balancing – Configured EC2 instances behind an ALB for high availability.  
- Database Access Management – Ensured private networking and restricted security policies for MySQL RDS.  
- Optimized Deployment Process – Streamlined infrastructure provisioning with reusable templates.  


## 📌 Conclusion  
This project helped me refine AWS CloudFormation skills, security configurations, and deployment automation for scalable cloud infrastructure. 🚀  
