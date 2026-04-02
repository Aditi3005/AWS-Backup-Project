# AWS-Backup-Project
This project demonstrates how to implement a centralized backup strategy using AWS Backup to protect critical cloud resources such as EC2 instances and RDS databases.  The goal is to prevent data loss by automating backup schedules, defining retention policies, and enabling recovery through backup vaults.

🎯 Objective
.Configure automated backups for:
   .Amazon EC2
   .Amazon RDS
.Create a centralized backup plan
.Validate backup and recovery points

🛠️ Services Used
.AWS Backup
.Amazon EC2
.Amazon RDS
.IAM (for permissions)

⚙️ Key Features
.Automated backup scheduling
.Centralized backup vault
.Resource tagging for backup assignment
.On-demand backup testing
.Recovery point validation

STEP:
Step1:Launch EC2 Instance
<img width="1918" height="1031" alt="Screenshot 2026-03-04 214201" src="https://github.com/user-attachments/assets/4eadf7cd-2924-4bb0-8031-7f8d0299b6d0" />

.sudo yum update -y
.sudo yum install httpd -y
.sudo systemctl start httpd
.echo " AWS Backup Test Page" > /var/www/html/index.html
<img width="1917" height="960" alt="Screenshot 2026-03-04 214300" src="https://github.com/user-attachments/assets/4c3db14c-2fd0-44fd-95ed-1a1497f93ebc" />

Step2:Create RDS Database
- Created RDS MySQL instance  
- Created database and table  
- Inserted sample data
  <img width="1919" height="1023" alt="Screenshot 2026-03-04 214229" src="https://github.com/user-attachments/assets/dea44db2-95b6-4ac4-8571-46f4b830d8cc" />




