# LAMPInstall
AWS AMI script to install LAMP.  Need Git to be installed

#Installing GIT
sudo yum install git
git clone https://github.com/joboyd4/LAMPInstall.git

#fstab needs to append with the following with updated UUID
UUID=542709a5-82dd-45b1-a521-8dac15a274a9       /var/www/html/myApps   ext4    defaults,nofail        0       2

#URL will be
IP address /myApps/myTestApp/
