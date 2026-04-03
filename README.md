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
    
  <img width="1913" height="955" alt="Screenshot 2026-03-07 155347" src="https://github.com/user-attachments/assets/4278f42f-c093-4d29-8785-1091ae16692a" />

- Created database and table  
- Inserted sample data
  
  <img width="1918" height="940" alt="Screenshot 2026-03-04 231716" src="https://github.com/user-attachments/assets/f8f5b433-dd0b-4f66-b56f-5c7cf8cc8dc6" />


 Step 3: Create Backup Vault
- Accessed AWS Backup service from AWS Console  
- Created a backup vault named `MyBackupVault`  
- Backup vault acts as a secure storage location for recovery points  
- Used this vault in the backup plan configuration  
 (Note: Screenshot not available)

Step4:Step 4: Create Backup Plan
- Created new backup plan  
- Backup frequency: Daily  
- Retention period: 7 days
  
  <img width="1904" height="975" alt="Screenshot 2026-03-07 155531" src="https://github.com/user-attachments/assets/11cd1f1b-cc5e-4613-a4f0-47e31f506936" />

  Step 5: Assign Resources
- Selected EC2 instance  
- Selected RDS database  
- Assigned to backup plan
   
<img width="1905" height="1018" alt="Screenshot 2026-03-07 161035" src="https://github.com/user-attachments/assets/d972cb9b-b654-4121-8d7f-d8c07a8a88ed" />

 Step 6: Run Backup Job
- Triggered on-demand backup  
- Verified backup job status
   
<img width="1916" height="1022" alt="Screenshot 2026-03-07 160100" src="https://github.com/user-attachments/assets/bf45b051-da24-40a2-b464-ea9528634088" />

 Step 7: Verify Recovery Points
- Checked backup vault  
- Verified recovery points for EC2 & RDS
  
<img width="1919" height="1023" alt="Screenshot 2026-03-07 160344" src="https://github.com/user-attachments/assets/95cc3750-4acb-4efc-b20c-7040ab10af15" />

 ✅ Result
- Backup jobs completed successfully  
- Recovery points created for EC2 and RDS  
- Data protection strategy implemented

  ⚠️ Challenges Faced
- IAM role issue  
- Resource selection confusion

  ✅ Solutions
- Used AWSBackupDefaultServiceRole  
- Verified resource assignment properly  


 📌 Conclusion
This project successfully demonstrates how to use AWS Backup for automated backup and recovery, ensuring data safety and disaster recovery readiness.
