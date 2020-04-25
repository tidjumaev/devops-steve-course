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

