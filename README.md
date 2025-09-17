📌 Overview

This project demonstrates how I launched and configured an Amazon EC2 instance to host a simple web application.

🛠️ AWS Services Used

EC2 – Virtual server instance

VPC & Security Groups – Networking and firewall rules

IAM – Access management

📂 Project Steps

Created an EC2 instance (Amazon Linux 2).

Configured Security Groups to allow SSH (port 22) and HTTP (port 80).

Connected to EC2 via SSH using key pair.

Installed Apache server and hosted a test webpage.

🔑 Key Learnings

How to launch and connect to an EC2 instance.

Security group rules for SSH and HTTP.

Basic web hosting on Linux EC2.

📜 Commands
# Connect to EC2
ssh -i "my-key.pem" ec2-user@ec2-public-ip  

# Install Apache server
sudo yum update -y  
sudo yum install httpd -y  
sudo systemctl start httpd  
