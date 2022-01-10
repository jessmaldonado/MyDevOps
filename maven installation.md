
Prerequisites:
1. Jenkins server

Install Maven on Jenkins 
Download maven packages https://maven.apache.org/download.cgi onto Jenkins server. In this case I am using /opt/maven as my installation directory 

  # Creating maven directory under /opt
  mkdir /opt/maven
  cd /opt/maven
  # downloading maven version 3.6.0
  wget http://mirrors.fibergrid.in/apache/maven/maven-3/3.6.0/binaries/apache-maven-3.6.0-bin.zip
  unzip /opt/maven/apache-maven-3.6.0-bin.zip
  
  Setup M2_HOME and M2 paths in .bash_profile of user and add these to path variable

  vi ~/.bash_profile
  M2_HOME=/opt/maven/apache-maven-3.6.0
  M2=$M2_HOME/bin
  PAHT=<Existing_PATH>:$M2_HOME:$M2

Check point
  mvn –version
  
Setup maven on Jenkins console

Install maven plugin without restart
Manage Jenkins > Jenkins Plugins > available > "Maven Invoker" "Maven Integration" 

Configure java path

Manage Jenkins > Global Tool Configuration > Maven
