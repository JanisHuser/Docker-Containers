FROM codercom/code-server:latest

RUN sudo apt-get update

RUN mkdir -p /home/coder/repos && \
	chown coder:coder -R /home/coder/repos

RUN sudo curl -sL https://deb.nodesource.com/setup_17.x -o nodesource_setup.sh
RUN sudo bash nodesource_setup.sh
RUN sudo apt-get install nodejs

RUN sudo npm install -g @angular/cli

VOLUME /home/coder/repos
WORKDIR /home/coder/repos
