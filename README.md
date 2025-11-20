# Jenkins Training

  Jenkins is a GUI Tool.

  1. Create a EC2 instance on AWS  
  2. Install Java (openjdk)  
     ```     sudo apt-get install fontconfig openjdk-21-jre     ```  
  3. Install Jenkins  
     3.1. wget jenkins key  
     ```
     wget -q -O - https://pkg.jenkins.io/jenkins.io.key | sudo apt-key add -
     ```  
     3.2. source the package  
     ```
     echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
      https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
      /etc/apt/sources.list.d/jenkins.list > /dev/null
     ```  
     3.3. system update  
     ```     sudo apt-get update     ```  
     3.4. install jenkins  
     ```     sudo apt-get install jenkins     ```  
  4. Enable port 8080 on security groups  
  5. Start and Enable jenkins  
     ```
     systemctl start jenkins
     systemctl enable jenkins
     ```
  6. Note the Admin password for the jenkins  
     ```sudo cat /var/lib/jenkins/secrets/initialAdminPassword```
  7. Open the browser:
     ``` http://<EC2 Instance Public IP>:8080     ```
  8. Install the required plugins

---
