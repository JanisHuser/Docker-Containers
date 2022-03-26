FROM jetbrains/teamcity-agent:2021.2.3-linux-sudo

RUN sudo apt-get update
RUN sudo apt-get install default-jre -y
RUN sudo apt-get install default-jdk -y
RUN sudo apt-get install openjdk-17-jre -y
RUN sudo apt-get install wget
RUN sudo apt-get install unzip
#RUN sudo apt-get install gradle -y

ENV GRADLE_VERSION=7.4
RUN wget https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip -P /tmp
RUN sudo unzip -d /opt/gradle /tmp/gradle-${GRADLE_VERSION}-bin.zip
RUN sudo ln -s /opt/gradle/gradle-${GRADLE_VERSION} /opt/gradle/latest
ENV GRADLE_HOME=/opt/gradle/latest

RUN curl -L https://services.gradle.org/distributions/gradle-2.4-bin.zip -o gradle-2.4-bin.zip

ENV JAVA_HOME /usr/lib/jvm/java-17-openjdk-arm64/bin

ENV PATH="${GRADLE_HOME}/bin:${PATH}"
