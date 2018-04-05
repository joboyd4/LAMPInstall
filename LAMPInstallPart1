#!/bin/bash
#Installing Apache and PHP
sudo yum update -y
sudo yum install -y httpd24 php70 mysql56-server php70-mysqlnd
sudo service httpd start
sudo chkconfig httpd on
chkconfig --list httpd
ls -l /var/www
sudo usermod -a -G apache ec2-user
echo "Need to Exit and Re-Login and then run LampInstallPart2"
