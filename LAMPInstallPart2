#!/bin/bash
#Ensuring proper groups are assigned
groups
#Setting up Elastic Block Storage
lsblk
sudo file -s /dev/xvdf
sudo mkfs -t ext4 /dev/xvdf
sudo mkdir /var/www/html/myApps
sudo mount /dev/xvdf /var/www/html/myApps
sudo cp /etc/fstab /etc/fstab.orig
echo "Please enter UUID listed above so Elastic Block Storage can be mounted on reboots"
read UUID
sudo echo "UUID=".$UUID."       /var/www/html/myApps   ext4    defaults,nofail        0       2" >> fstab
df
sudo file -s /dev/xvdf
sudo mount -a
#Setting permissions for apache server directories
sudo chown -R ec2-user:apache /var/www
sudo chmod 2775 /var/www
find /var/www -type d -exec sudo chmod 2775 {} \;
find /var/www -type f -exec sudo chmod 0664 {} \;
sudo yum list installed httpd24 php70 mysql56-server php70-mysqlnd
#Setting up mySQLServer
sudo service mysqld start
sudo mysql_secure_installation
sudo chkconfig mysqld on
#Set myApps path
myApps=/var/www/html/myApps
cd $myApps
#Download myTestApp
git clone https://github.com/joboyd4/myTestApp.git
