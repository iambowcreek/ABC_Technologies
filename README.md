# abc_technologies
Edureka Project 1

Building a CI/CD Pipeline for a Retail Company - ABC Technologies.
Goals:
•	Highly Available 
•	Highly scalable 
•	Highly performant
•	Easily built and maintained
•	Developed and deployed quickly 
•	Lower production bugs 
•	Frequent releases 

Prerequisites:
•	Java
•	Maven
•	Git
•	Jenkins
•	Docker
•	Ansible
•	Kubernetes
•	Grafana 
•	Prometheus  

My Approach:
Steps:
•	Cloned the project SRC from GitHub Link to Local Machine 
•	Created a new GitHub repo: link https://github.com/iambowcreek/abc_technologies.git 
•	Initiated Git in Local Machine 
•	Pushed the SRC to the New Repo Created on GitHub 
•	Servers provisioned - 3 Servers for the following integration (Server A: Jenkins Master, Ansible Master, Docker. Server B: K8s Master, Ansible Node, Docker. Server C: K8s Node
•	Server A: Configured Jenkins and installed all necessary plugins for the pipeline integration, Installed Ansible – configured the node for communication in server B, installed docker and integrated it with Jenkins, integrated ansible with docker and K8S. 
•	Server B: Installed K8S, joined the node in server C. Created Ansible user and configured SSH connection with master node is server A. Installed Docker. 
•	Server C: K8S Node 1 configured.
•	Created my CI/CD Pipeline in Jenkins and configured My Jenkins Configurations with Maven Tool.
•	Created my Jenkinsfile for my CI/CD Pipeline
•	Executed the Maven commands using Jenkinsfile – compile, test and package.
•	Configured my Pipeline Build triggers and GitHub Webhook.
•	Configured Docker and Ansible in Jenkins Global Tool Configuration.
•	Created a new Docker repo for my image in Dockerhub - https://hub.docker.com/repository/docker/iambowcreek/abc_technologies/general 
•	Created my Dockerfile on my local machine using VSCode and pushed to my GitHub repo to trigger build. 
•	Updated my Jenkinsfile to build Docker images with Tomcat as the base image and push to Dockerhub 
•	Configured K8S cloud on Jenkins
•	Created my Ansible Playbook to deploy ABC Technologies Artifacts to K8S – deployment and service 
•	Updated my Jenkinsfile to execute Ansible Playbook to deploy my containerised application to K8S server. 

