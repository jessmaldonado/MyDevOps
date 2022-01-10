### Prerequisites
EC2 instance with Java v1.8.x

### Install Java
1. Get the latest version from http://openjdk.java.net/install/
```sh
yum install java-1.8*
#yum -y install java-1.8.0-openjdk-devel
```
1. Set the JAVA HOME
```sh
java -version
find /usr/lib/jvm/java-1.8* | head -n 3
```
##### To set it permanently update your .bash_profile
```sh
nano ~/.bash_profile

JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.312.b07-1.amzn2.0.2.x86_64
export JAVA_HOME
PATH=$PATH:$JAVA_HOME
```

3. Confirm Java Version and set the java home. The output should be something like this:
 ```sh
[root@~]# java -version
openjdk version "1.8.0_312"
OpenJDK Runtime Environment (build 1.8.0_312-b07)
OpenJDK 64-Bit Server VM (build 25.312-b07, mixed mode)
```

### Install Apache Tomcat
1. Donwload tomcat packages from:   not /opt on EC2 instance
```sh
# Create tomcat directory
cd /opt
wget https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.73/bin/apache-tomcat-8.5.73.tar.gz
tar -xvzf /opt/apache-tomcat-8.5.73.tar.gz
```

2. Grant executin permissions to start.sh and shutdown.sh which are under bin dir
```sh
chmod -x opt/apache-tomcat-8.5.35/bin/startup.sh 
shutdown.sh
```
 
