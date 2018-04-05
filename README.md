# LAMPInstall
AWS AMI script to install LAMP.  Need Git to be installed

#Installing GIT
sudo yum install git
git clone https://github.com/joboyd4/LAMPInstall.git

#SQLServer Install
When prompted, type a password for the root account.

Type the current root password. By default, the root account does not have a password set. Press Enter.

Type Y to set a password, and type a secure password twice. For more information about creating a secure password, see https://identitysafe.norton.com/password-generator/. Make sure to store this password in a safe place.

Note

Setting a root password for MySQL is only the most basic measure for securing your database. When you build or install a database-driven application, you typically create a database service user for that application and avoid using the root account for anything but database administration.

Type Y to remove the anonymous user accounts.

Type Y to disable the remote root login.

Type Y to remove the test database.

Type Y to reload the privilege tables and save your changes.

#URL will be
IP address /myApps/myTestApp/
