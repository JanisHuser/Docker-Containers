FROM codercom/code-server:latest


RUN mkdir -p /home/coder/repos && \
	chown coder:coder -R /home/coder/repos



RUN sudo apt-get update
RUN sudo apt-get install default-jre -y
RUN sudo apt-get install default-jdk -y
RUN sudo apt-get install openjdk-17-jre -y
#RUN sudo apt-get install gradle -y

ENV GRADLE_VERSION=6.5.1
RUN wget https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip -P /tmp
RUN sudo unzip -d /opt/gradle /tmp/gradle-${GRADLE_VERSION}-bin.zip
RUN sudo ln -s /opt/gradle/gradle-${GRADLE_VERSION} /opt/gradle/latest
ENV GRADLE_HOME=/opt/gradle/latest

RUN curl -L https://services.gradle.org/distributions/gradle-2.4-bin.zip -o gradle-2.4-bin.zip

VOLUME /home/coder/repos
WORKDIR /home/coder/repos


ENV JAVA_HOME /usr/lib/jvm/java-17-openjdk-arm64/bin
