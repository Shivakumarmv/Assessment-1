
# Prerequisites

AWS Account

# A Step-by-step guide

login to aws console and type ec2 in the AWS console. and click on ec2 service 

![Screenshot 2024-11-06 141850](https://github.com/user-attachments/assets/fe9e7543-5823-44e9-acad-f92823fd440f)



Click on the instance button and then click on the Launch Instance button on the top right corner.

![Screenshot 2024-11-06 143957](https://github.com/user-attachments/assets/24de38c4-403b-49b1-973b-6da93d059c06)


here we can see the form where we can fill the configuration of instance. please enter the name that you want to keep.

![Screenshot 2024-11-06 144313](https://github.com/user-attachments/assets/0ba291fc-444b-46da-8156-c153309579f3)


select os which you what in my case Amazon Linux and Select instance type t2.micro

![Screenshot 2024-11-06 145016](https://github.com/user-attachments/assets/cf9dc74d-25a0-41f7-a32e-0b2738f82611)



Scroll down, create new key pair and enter name for the key pair and click create key pair and attach key pair 

![Screenshot 2024-11-06 145622](https://github.com/user-attachments/assets/678e22c6-8005-4ca8-8814-182a820b23ee)

![Screenshot 2024-11-06 150158](https://github.com/user-attachments/assets/601f355f-ecea-446d-babe-b938dbfe1a4d)


In network settings we can use the default VPC given by AWS. In short, keep the Network setting as it is. In the firewall setting select all the fields as I shown in the below image to keep things simple.

![Screenshot 2024-11-06 145704](https://github.com/user-attachments/assets/87b88613-4a28-4df6-b448-12335b42e2c2)


# ssh to server

Navigate to instance page and select instance recently launched and click on connect button top 

![Screenshot 2024-11-07 150759](https://github.com/user-attachments/assets/34d6ea4a-c8d3-4562-9637-b21e2603d24c)


Scroll down and click connect button 

![Screenshot 2024-11-06 150908](https://github.com/user-attachments/assets/3c61b54a-fd60-4a64-be71-da8a34db8690)




# Change to root user

```
sudo su -

```
![Screenshot 2024-11-06 154727](https://github.com/user-attachments/assets/004fba0f-e8e0-44a2-ae3d-86392381aa05)

# Install git and apache server

```

yum install git -y 
yum install httpd -y

```

![Screenshot 2024-11-06 154615](https://github.com/user-attachments/assets/f8f464c3-d73f-46da-a9b1-54611afa0fdc)



# Start the service and change directory 

```
systemctl start httpd
systemctl status httpd

cd /var/www/html

```

![Screenshot 2024-11-06 155356](https://github.com/user-attachments/assets/f57f70f3-f8ec-44fa-abb9-abd9de47aa41)


# upload or build from scratch

![Screenshot 2024-11-07 122235](https://github.com/user-attachments/assets/09e95f76-95b3-49b1-968b-34dca1877e71)




# Testing

select server and copy the public ip address and paste in browser 
If we can see the website in fully functional mode, it means we have properly set up and configured 

![Screenshot 2024-11-06 160752](https://github.com/user-attachments/assets/55480df9-8f95-4373-9c3b-7643458220a8)


# Create a repository in github

![Screenshot 2024-11-06 161127](https://github.com/user-attachments/assets/d7774612-6369-41d2-895d-75eb6c0ea902)

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
![Screenshot 2024-11-06 161236](https://github.com/user-attachments/assets/ce1920a8-d3c1-4c70-90b9-1b30b22ad4d6)

![Screenshot 2024-11-06 161456](https://github.com/user-attachments/assets/c09b20c3-ce0f-4926-a29b-07169ec469ab)



# Authentication

Generate token from github -> go to github -> settings -> developer settings ->personal access token -> tokens (classic) -> generate token

![Screenshot 2024-11-06 161825](https://github.com/user-attachments/assets/b314f705-9208-42f9-998c-11abaa2f1b4b)
