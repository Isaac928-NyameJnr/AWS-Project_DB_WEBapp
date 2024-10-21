# AWS-Project_DB_WEBapp
Project Title
-Host a web application using AWS EC2 and connected with Aurora MySQL free tier.
Project Description

This project adheres to the principles of the AWS Well-Architected Framework.

Security Principle: I restricted SSH traffic to only allow access from my specific IP address. This ensures that only my device can access the instance, protecting it from unauthorized access and safeguarding it from potential threats.

Cost Optimization Principle: To minimize unnecessary costs, I selected the burstable instance class option. This choice is suitable for the project's workload, which does not require high-performance resources, thus preventing excess spending.

Reliability Principle: A manual snapshot of the database was created to serve as a backup, ensuring disaster recovery and protecting against data loss.

Steps to Set Up the Web Application
-Create EC2 instance:
-Make sure to allow SSH traffic only from your IP for secure access.

-Create the Database
-Select Aurora(MySql Compatible) and proceed with needed configurations

SSH into EC2 instance:
-Use the command:
ssh -i /path/to/your-key.pem ec2-user@your-ec2-public-ip
-Update and install required software:
sudo dnf update -y
sudo dnf install -y httpd php php-mysqli mariadb105

Start Apache web server:
sudo systemctl start httpd

Upgrade the web app:
-Create a folder and set proper permissions.
-Create the following files:
-dbinfo.inc: To store database connection details.
-SamplePage.php: To contain HTML and PHP code for web app functionality.

Download and install MySQL client on your EC2 instance:
sudo yum install https://dev.mysql.com/get/mysql80-community-release-el7-3.noarch.rpm -y
sudo yum install mysql-community-client -y

Connect to the Aurora MySQL DB:
mysql -h database-1-instance-1-eu-north-1a.cn6ysks4wg8e.eu-north-1.rds.amazonaws.com -P 3306 -u admin -p
Database endpoint:

