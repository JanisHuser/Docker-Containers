FROM codercom/code-server:latest


RUN mkdir -p /home/coder/repos && \
	chown coder:coder -R /home/coder/repos

RUN curl -sL https://deb.nodesource.com/setup_10.x -o nodesource_setup.sh

RUN bash nodesource_setup.sh
RUN sudo apt-get install nodejs


RUN npm install -g @angular/cli

VOLUME /home/coder/repos
WORKDIR /home/coder/repos
