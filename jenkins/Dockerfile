FROM jenkins/jenkins:lts

USER root

RUN apt-get update && apt-get install -y wget unzip

RUN wget https://dlcdn.apache.org/maven/maven-3/3.9.11/binaries/apache-maven-3.9.11-bin.zip -P /tmp && \
    unzip /tmp/apache-maven-3.9.11-bin.zip -d /opt && \
    ln -s /opt/apache-maven-3.9.11 /opt/maven && \
    rm /tmp/apache-maven-3.9.11-bin.zip

ENV MAVEN_HOME=/opt/maven
ENV PATH=${MAVEN_HOME}/bin:${PATH}

USER jenkins
