# django
#!/bin/bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
sudo yum install python3 -y
sudo pip3 install django
sudo pip3 install psycopg2-binary
sudo pip3 install pillow
mkdir django
cd django
aws s3 sync s3://akmanai /home/ec2-user/django
