# aws_CICD
aws cicd pipelines, codedeploy, git, ec2 instance 

user_data for ec2_instance

#!/bin/bash
sudo yum -y update
sudo yum -y install ruby
sudo yum -y install wget
cd /home/ec2-user
wget https://<bucket-name>.s3.<region-identifier>.amazonaws.com/latest/install
sudo chmod +x ./install
sudo ./install auto
sudo yum install -y python-pip
sudo pip install awscli

Reference: https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-ec2-create.html
https://docs.aws.amazon.com/codedeploy/latest/userguide/resource-kit.html#resource-kit-bucket-names

workflows: https://github.com/ThanHtutPC/aws_CICD/blob/main/Untitled-2024-05-23-0158.png

Recommanded 
Please read the README.txt file first.

Create the ec2 instance and install the requirement application. 
Deploy the pipeline and attach with github(version2)
Deploy the CodeDeploy and create the development group.
call your website EX. (your_ec2_public_IP)
