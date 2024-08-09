## mysql ##

Install mysql database on AWS EC2 Linux

sudo wget https://dev.mysql.com/get/mysql80-community-release-el9-1.noarch.rpm

sudo dnf install mysql80-community-release-el9-1.noarch.rpm -y

sudo rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-2023

sudo dnf install mysql-community-client -y

sudo dnf install mysql-community-server -y

sudo systemctl start mysqld

cat /var/log/mysqld.log | grep "password"

sudo mysql_secure_installation

enter tempory password & set new password

sudo mysql -u root -p    (login mysql with new password)
