Insta java

sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install -y fontconfig openjdk-17-jre openjdk-17-jdk
_________________________________________________________________________________________

install maven

cd /tmp ; sudo wget https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz
cd /tmp ; sudo tar -xzf apache-maven-3.9.6-bin.tar.gz -C  /opt/
mv /opt/apache-maven-3.9.6 /opt/maven
sudo echo "MAVEN_HOME=\"/opt/maven\"" >> /etc/profile
sudo echo "PATH=\$MAVEN_HOME/bin:\$PATH" >> /etc/profile
source /etc/profile

_____________________________________________________________________________________

install Jenkins

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
____________________________________________________________________________________________________

terraform
sudo wget https://raw.githubusercontent.com/lerndevops/labs/master/scripts/installTerraform.sh -P /tmp
sudo chmod 755 /tmp/installTerraform.sh
sudo bash /tmp/installTerraform.sh
