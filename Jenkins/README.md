## <img src="https://www.jenkins.io/images/logos/jenkins/jenkins.png" alt="Jenkins Logo" width="30"/> **Difference between Continuous Integration and Continuous Deployment**


<img src="https://www.novelvista.com/resources/images/blogs/details/what-is-continuous-deployment-delivery.webp" alt="Continuous Deployment vs. Delivery" width="500"/>


sudo yum install epel-release -y
sudo yum install fontconfig java-17-openjdk -y

sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo --no-check-certificate      #install jenkins
sudo rpm --import http://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
sudo yum install jenkins -y

sudo vi /lib/systemd/system/jenkins.service    #change port

sudo systemctl start jenkins   #starts jenkins service
