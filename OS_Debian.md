#安装sudo
su  
apt-get install sudo

#安装yum
sudo apt-get update  
sudo apt-get install build-essential  
sudo apt-get install yum  

#安装Jenkins
###获取docker image
docker pull jenkins/jenkins  
### 创建数据目录 (jenkins root folder)
mkdir /data/devops/jenkins

### 启动jenkins 
docker run -d -p 8080:8080 -p 50000:50000 -v /data/devops/jenkins:/var/jenkins_home -v /etc/localtime:/etc/localtime --name jenkins-server jenkins/jenkins
