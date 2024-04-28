##STEPS FOR SETTINGUP JENKINS
- Install Java
  sudo apt install openjdk-17-jre-headless
- Install Jenkins
  sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
    https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
  echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
    https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null
  sudo apt-get update
  sudo apt-get install jenkins

##STEPS FOR SETTINGUP DOCKER
- Install Docker
  sudo apt  install docker.io -y
- Grant users on the system to read from and write to the Docker socket, which can be useful for allowing non-root users to run Docker commands.
  sudo chmod 666 /var/run/docker.sock
 
