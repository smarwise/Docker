FROM debian
ENV TS3SERVER_LICENSE=accept
RUN apt-get update && apt-get upgrade
RUN apt-get install -y wget
RUN apt-get install -y bzip2
RUN apt-get install -y systemd
RUN apt-get install -y nano
RUN apt-get install -y sudo
RUN adduser --disabled-login teamspeak
RUN cd /home/teamspeak
RUN wget http://dl.4players.de/ts/releases/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2
RUN tar xvf teamspeak3-server_linux_amd64-3.8.0.tar.bz2
RUN cd teamspeak3-server_linux_amd64 && ./ts3server_minimal_runscript.sh start
