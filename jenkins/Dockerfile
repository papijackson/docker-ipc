FROM jenkins

USER root
RUN apt-get update && apt-get install wget
# get maven 3.5.0
RUN wget --no-verbose -O /tmp/apache-maven-3.5.0-bin.tar.gz http://mirrors.standaloneinstaller.com/apache/maven/maven-3/3.5.0/binaries/apache-maven-3.5.0-bin.tar.gz
# install maven
RUN tar xzf /tmp/apache-maven-3.5.0-bin.tar.gz -C /opt/
RUN ln -s /opt/apache-maven-3.5.0 /opt/maven
RUN ln -s /opt/maven/bin/mvn /usr/local/bin
RUN rm -f /tmp/apache-maven-3.5.0.tar.gz
ENV MAVEN_HOME /opt/maven

USER jenkins