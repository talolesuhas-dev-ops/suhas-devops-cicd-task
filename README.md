Project Title: Automated Website Deployment using Jenkins and Docker
Created a CI/CD pipeline using Jenkins. Integrated GitHub with Jenkins for automatic code deployment. Built and deployed Docker containers on AWS EC2. Automated application deployment process, reducing manual effort. Managed Linux server and Docker containers.

Project Objective:
The goal of this project is to automatically deploy a website whenever new code is pushed to GitHub. Instead of manually copying files to the server, the entire process is automated using DevOps tools.

Tools Used :
Git GitHub Jenkins Docker AWS EC2 Linux (Ubuntu)

Project Workflow :
Step 1: Create Website Create a simple HTML/CSS website.

Step 2: Push Code to GitHub Store the website code in a GitHub repository.

Step 3: Configure Jenkins Install Jenkins on an EC2 server and connect it with GitHub.

Step 4: Build Docker Image Whenever code is pushed to GitHub, Jenkins automatically builds a Docker image.

Step 5: Deploy Container Jenkins deploys the Docker container on AWS EC2.

Step 6: Access Website Users can access the website through the EC2 public IP.

Architecture
Developer -> Github -> Jenkins -> Docker Build -> AWS EC2 -> Website Live.

Commands Used During Project :
install Docker:

sudo apt update sudo apt install docker.io -y sudo systemctl start docker sudo systemctl enable docker

Install Jenkins:

sudo apt update

sudo apt install openjdk-17-jdk -y

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]
https://pkg.jenkins.io/debian-stable binary/ | sudo tee
/etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install jenkins -y

Start Jenkins :

sudo systemctl start jenkins sudo systemctl enable jenkins

Features
Continuous Integration
Continuous Deployment
Automated Docker Build
Automated Application Deployment
Version Control using GitHub
Setup Steps
Clone Repository

git clone https://github.com/talolesuhas-dev-ops/suhas-devops-cicd-task.git
Build Docker Image

docker build -t devops-website .
Run Container

docker run -d -p 80:80 devops-website
Learning Outcomes
CI/CD Pipeline Implementation
Jenkins Automation
Docker Containerization
AWS EC2 Deployment
GitHub Integration
