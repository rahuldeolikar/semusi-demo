# semusi-demo
this is semusi-demo-repo

# Step 1
create one repo exmple semusi-demo on github
url:- https://github.com/rahuldeolikar/semusi-demo.git

create a file index.html and insert semusi-demo

# step 2
create two instance one is jenkins-master
key add
ami ubuntu
security group 8080,22 port allow

# 2nd is Nginx-ws-dep
Nginx 
ami ubuntu
key pair
sg 8080,22 port allow
after that access jenkins server with the help of SSH.

Add jenkins 
# sudo apt update
# sudo apt install openjdk-17-jre

# curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

# You can enable the Jenkins service to start at boot with the command:

sudo systemctl enable jenkins
You can start the Jenkins service with the command:

sudo systemctl start jenkins
You can check the status of the Jenkins service using the command:

sudo systemctl status jenkins

# step 4
login jenkins server
add password 

install jenkins plugin
# node and leble parameter

# step 5 
after that add ssh key
add credensials

create node
for nginx web app

# step 6
go to manage jenkins
select node
create node

now create job
restric where this project can be run 
Node

for source code management add git repo url: https://github.com/rahuldeolikar/semusi-demo.git

# step 7

Branch specify ---> main

Build steps
 Execute shell
             /home/ubuntu/workspace/semusi-web-app/index.html /var/www/html/

save and apply

then hit ip
http://52.90.241.120/

Welcome to semusi "Hello World"

Thank You
