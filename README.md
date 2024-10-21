# AWS-Project_DB_WEBapp
Project Overview
-Hosted a web application using AWS EC2 and Aurora MySQL.

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

