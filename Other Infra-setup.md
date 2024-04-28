# Project Setup Guide

## Steps for Setting Up Jenkins

### Install Java

```bash
sudo apt install openjdk-17-jre-headless

### Install Jenkins
```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
    https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
    https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

## Steps for Setting Up Docker

### Install Docker
```bash
sudo apt install docker.io -y

## Grant Users Access to Docker Socket
To allow non-root users to run Docker commands, grant them read and write access to the Docker socket.
```bash
sudo chmod 666 /var/run/docker.sock

## Delete the Kubernetes Cluster
```bash
eksctl delete cluster --name EKS-1 --region eu-north-1






