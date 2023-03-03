FROM giddu/jenkins-inbound-agent:awscli

USER root

RUN apt-get update && apt-get install -y wget

RUN wget https://packages.microsoft.com/config/debian/11/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN rm packages-microsoft-prod.deb

RUN apt-get update && \
      apt-get install -y dotnet-sdk-6.0

RUN apt-get install openjdk-11-jdk -y
 
RUN update-alternatives --config java 

USER jenkins

RUN dotnet tool install --global dotnet-sonarscanner