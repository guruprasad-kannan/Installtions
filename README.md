# Installing Jenkins on Amazon Linux:
#!/bin/sh

sudo amazon-linux-extras install java-openjdk11 -y

amazon-linux-extras install epel -y

yum update -y

wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins.io/redhat-stable/jenkins.repo

rpm --import http://pkg.jenkins.io/redhat-stable/jenkins.io.key

yum install jenkins –y

systemctl start jenkins
