
# Prerequisites

AWS Account

# A Step-by-step guide

login to aws console and type ec2 in the AWS console. and click on ec2 service 

![Screenshot 2024-11-06 141850](https://github.com/user-attachments/assets/1855ee0c-1ccd-4ced-8136-4d5db34c08eb)


Click on the instance button and then click on the Launch Instance button on the top right corner.

![Screenshot 2024-11-06 143957](https://github.com/user-attachments/assets/a23f679f-0f13-476e-a5ff-e5647517c548)


here we can see the form where we can fill the configuration of instance. please enter the name that you want to keep.

![Screenshot 2024-11-06 144313](https://github.com/user-attachments/assets/a0e70b98-3b7d-4f83-a696-db0d54a47a2d)


select os which you what in my case Amazon Linux and Select instance type t2.micro

![Screenshot 2024-11-06 145016](https://github.com/user-attachments/assets/8965dd1b-0219-4785-bed5-b0d886f69b90)


Scroll down, create new key pair and enter name for the key pair and click create key pair and attach key pair 

![Screenshot 2024-11-06 145622](https://github.com/user-attachments/assets/d10f28e4-d734-48f7-8f7a-c515c3d31f97)

![Screenshot 2024-11-06 150158](https://github.com/user-attachments/assets/5c01d443-52fe-4ed4-8916-cc7bc090ada0)


In network settings we can use the default VPC given by AWS. In short, keep the Network setting as it is. In the firewall setting select all the fields as I shown in the below image to keep things simple.

![Screenshot 2024-11-06 145704](https://github.com/user-attachments/assets/81b688b9-cda7-492d-9e10-e42a7078b364)



# Change to root user

```
sudo su -

```
![Screenshot 2024-11-06 154727](https://github.com/user-attachments/assets/2dbc112e-8103-470d-b036-b82cb6e6adbf)

# Install git and apache server

```

yum install git -y 
yum install httpd -y

```

![Screenshot 2024-11-06 154615](https://github.com/user-attachments/assets/ef3ba15c-3c03-4aca-937e-d7f7afede9eb)


# Start the service and change directory 

```
systemctl start httpd
systemctl status httpd

cd /var/www/html

```
![Screenshot 2024-11-06 155356](https://github.com/user-attachments/assets/77afe8eb-d431-455a-932a-e992b9980613)


# upload or build from scratch


![Screenshot 2024-11-07 122235](https://github.com/user-attachments/assets/7184d5f2-c160-4559-8bed-c1a3b77a6507)


# Testing

select server and copy the public ip address and paste in browser 
If we can see the website in fully functional mode, it means we have properly set up and configured 

![Screenshot 2024-11-06 160752](https://github.com/user-attachments/assets/11f81d7f-24ca-4e0a-8f40-b6d3d4831a1b)

# Create a repository in github

![Screenshot 2024-11-06 161127](https://github.com/user-attachments/assets/9ce0ef8d-073a-460e-ae2f-9d2310a06d78)

# initialize a Git repository and the Remote Repository 

```
git init
git add .
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Shivakumarmv/Assessment-1.git
git push -u origin main

```

![Screenshot 2024-11-06 161236](https://github.com/user-attachments/assets/b7b05b6d-90cd-4776-bfaa-04f192e62a20)


![Screenshot 2024-11-06 161825](https://github.com/user-attachments/assets/f713e4dc-ded9-407c-a6c6-8a13c90075e4)



# Authentication

Generate token from github -> go to github -> settings -> developer settings ->personal access token -> tokens (classic) -> generate token

![Screenshot 2024-11-06 161456](https://github.com/user-attachments/assets/b51dc3e4-3fff-4315-9671-83e888c00aee)
