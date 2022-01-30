FROM codercom/code-server:latest


RUN mkdir -p /home/coder/repos && \
	chown coder:coder -R /home/coder/repos



RUN sudo apt-get update
RUN sudo apt-get install default-jre -y
RUN sudo apt-get install default-jdk -y
RUN sudo apt-get install openjdk-17-jre -y
RUN sudo apt-get install gradle -y

VOLUME /home/coder/repos
WORKDIR /home/coder/repos
