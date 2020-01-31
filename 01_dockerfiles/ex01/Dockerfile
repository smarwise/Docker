FROM debian

RUN apt-get update && apt-get upgrade
RUN apt-get install -y wget
RUN apt-get install -y bzip2
RUN apt-get install -y systemd
RUN apt-get install -y nano
RUN apt-get install -y sudo
RUN adduser --disabled-login teamspeak
RUN cd /home/teamspeak
RUN wget http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2
RUN tar xjvf teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2

WORKDIR /teamspeak3-server_linux_amd64

ENV TS3SERVER_LICENSE=accept
RUN ./ts3server_minimal_runscript.sh start