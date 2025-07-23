# <img src="https://www.jenkins.io/images/logos/jenkins/jenkins.png" alt="Jenkins Logo" width="30"/> **Jenkins Setup & CI/CD Concepts**

---
###   Difference between **Continuous Integration** and **Continuous Deployment**

### 📊 Visual Representation

<p align="center">
  <img src="https://www.novelvista.com/resources/images/blogs/details/what-is-continuous-deployment-delivery.webp" alt="Continuous Deployment vs Delivery" width="600"/>
</p>

---

### ⚙️ Jenkins Installation on RHEL/CentOS

Follow the steps below to install Jenkins:

#### 🔧 Step 1: Install Required Packages

```bash
sudo yum install epel-release -y
sudo yum install fontconfig java-17-openjdk -y
```
#### 📥 Step 2: Add Jenkins Repository and Import Key

```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo --no-check-certificate
sudo rpm --import http://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```
#### 📦 Step 3: Install Jenkins

```bash
sudo yum install jenkins -y
```
#### 🛠️ Step 4: Change Jenkins Port (Optional)

To change the default port from 8080 to something else:
```bash
sudo vi /lib/systemd/system/jenkins.service
Find and modify:
```
> --httpPort=8080 → --httpPort=YOUR_PORT

#### ▶️ Step 5: Start Jenkins Service

```bash
sudo systemctl start jenkins
```

#### 🌐 Access Jenkins
Once Jenkins is up and running, visit it in your browser:
```bash
http://(your-server-ip):8080
```

🔐 Get the Initial Admin Password:
```bash

sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

#### ✅ Final Checklist
 - Java installed
 - Jenkins installed
 - Service running
 - Accessible via browser
 - Admin password retrieved
   
💡 Tip: Ensure firewall rules allow traffic on the Jenkins port (default is 8080).
