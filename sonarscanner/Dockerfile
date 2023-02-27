FROM giddu/jenkins-inbound-agent:awscli

USER root

ENV SONAR_SCANNER_VERSION=4.8.0.2856
RUN mkdir /opt/sonarscanner && \
  cd /opt/sonarscanner && \
  curl https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-${SONAR_SCANNER_VERSION}-linux.zip -o "sonar-scanner-cli.zip" && \
  unzip sonar-scanner-cli.zip && \
  rm sonar-scanner-cli.zip && \
  chmod +x sonar-scanner-${SONAR_SCANNER_VERSION}-linux/bin/sonar-scanner && \
  ln -s /opt/sonarscanner/sonar-scanner-${SONAR_SCANNER_VERSION}-linux/bin/sonar-scanner /usr/local/bin/sonar-scanner

USER jenkins
