# EC2 Project: Launch and Configure an EC2 Instance

📌 Overview

This project demonstrates how I launched and configured an Amazon EC2 instance to host a simple web application.

---

## 🛠️ AWS Services Used

- EC2 – Virtual server instance
- VPC & Security Groups – Networking and firewall rules
- IAM – Access management

---

## ⚡ Prerequisites

- AWS account with permissions to create EC2 instances
- SSH key pair for connecting to your instance
- Basic knowledge of AWS Console

---

## 🚀 Getting Started

1. Launch EC2 Instance
   - Select Amazon Linux 2 AMI
   - Choose an instance type (e.g., t2.micro)
   - Create or select an SSH key pair

2. Configure Security Groups
   - Allow inbound SSH (port 22) and HTTP (port 80)

3. Connect to EC2 via SSH
   ```bash
   ssh -i "my-key.pem" ec2-user@<EC2_PUBLIC_IP>
   ```

4. Install Apache Web Server
   ```bash
   sudo yum update -y
   sudo yum install httpd -y
   sudo systemctl start httpd
   ```

5. Host Test Webpage
   - Place an `index.html` file in `/var/www/html`:
     ```bash
     echo "<h1>Hello from EC2!</h1>" | sudo tee /var/www/html/index.html
     ```

---

## ✅ Output

After completing the steps, visit `http://<EC2_PUBLIC_IP>` in your browser.  
You should see:

```
Hello from EC2!
```

---

## 📚 Key Learnings

- How to launch and connect to an EC2 instance
- Configuring security group rules for SSH and HTTP
- Basic web hosting on Amazon Linux EC2

---

## 👤 Author & License

**Author:** syedafnan17  
**License:** MIT