# EC2-Project-Launch-and-Configure-an-EC2-Instance

# Connect to EC2
ssh -i "my-key.pem" ec2-user@ec2-public-ip  

# Install Apache server
sudo yum update -y  
sudo yum install httpd -y  
sudo systemctl start httpd  
