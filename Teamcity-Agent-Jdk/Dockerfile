FROM vlrpi/teamcity-agent:ubuntu-bionic-2020.2

RUN sudo apt-get update
RUN sudo apt-get install default-jre -y
RUN sudo apt-get install default-jdk -y
RUN sudo apt-get install openjdk-17-jre -y
RUN sudo apt-get install wget
RUN sudo apt-get install unzip
#RUN sudo apt-get install gradle -y

ENV GRADLE_VERSION=6.5.1
RUN wget https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip -P /tmp
RUN sudo unzip -d /opt/gradle /tmp/gradle-${GRADLE_VERSION}-bin.zip
RUN sudo ln -s /opt/gradle/gradle-${GRADLE_VERSION} /opt/gradle/latest
ENV GRADLE_HOME=/opt/gradle/latest

RUN curl -L https://services.gradle.org/distributions/gradle-2.4-bin.zip -o gradle-2.4-bin.zip

ENV BUILD_AGENT_NAME=RpiJanis
ENV SERVER_URL=http://ateastarathome.ddns.net:8090

ENV JAVA_HOME /usr/lib/jvm/java-17-openjdk-arm64/bin
