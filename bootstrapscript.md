# BootStrapScript

## \#!/bin/bash

yum update -y   
yum install httpd -y   
service httpd start   
chkconfig httpd on   
cd /var/www/html   
echo "Hello Cloud Gurus Welcome To My Webpage" &gt; index.html   
aws s3 mb s3://YOURBUCKETNAMEHERE   
aws s3 cp index.html s3://YOURBUCKETNAMEHERE

## \#!/bin/bash

yum install httpd php php-mysql -y   
cd /var/www/html   
wget [https://wordpress.org/wordpress-5.1.1.tar.gz](https://wordpress.org/wordpress-5.1.1.tar.gz)   
tar -xzf wordpress-5.1.1.tar.gz   
cp -r wordpress/\* /var/www/html/   
rm -rf wordpress   
rm -rf wordpress-5.1.1.tar.gz   
chmod -R 755 wp-content   
chown -R apache:apache wp-content   
service httpd start   
chkconfig httpd on

