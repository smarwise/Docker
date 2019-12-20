FROM debian

ENV TS3SERVER_LICENSE=accept
ENV VERSION=3.3.1

RUN apt-get update
RUN apt-get install -y bzip2
RUN apt-get install -y wget
RUN wget http://dl.4players.de/ts/releases/3.3.1/teamspeak3-server_linux_amd64-${VERSION}.tar.bz2
RUN tar -jxvf ./*.bz2

ENTRYPOINT ["./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]
