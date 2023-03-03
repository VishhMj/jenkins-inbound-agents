FROM giddu/jenkins-inbound-agent:awscli

USER root

RUN apt-get update && apt-get -y install sudo

RUN sudo apt update && sudo apt install git

RUN sudo apt update && sudo apt -y install dotnet6

RUN export PATH="$PATH:/root/.dotnet/tools"

RUN sudo apt-get install openjdk-11-jdk -y

RUN sudo apt-get install openjdk-11-jre -y
 
RUN sudo update-alternatives --config java 


USER jenkins

RUN dotnet tool install --global dotnet-sonarscanner

RUN dotnet tool list --global