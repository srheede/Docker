FROM debian:latest
RUN apt-get -y update && \
	apt-get -y upgrade && \
	apt install -y wget && \
	apt install -y bzip2 && \
    wget http://dl.4players.de/ts/releases/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2 &&\
    tar xvf teamspeak3-server_linux_amd64-3.8.0.tar.bz2 &&\
    rm -rf teamspeak3-server_linux_amd64-3.8.0.tar.bz2 &&\
    cd teamspeak3-server_linux_amd64 &&\
    touch .ts3server_license_accepted
ENV TS3SERVER_LICENSE=accept
EXPOSE  9987/udp 10011 30033
ENTRYPOINT ./ts3server_minimal_runscript.sh start