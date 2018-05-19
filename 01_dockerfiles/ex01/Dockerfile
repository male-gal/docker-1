FROM debian:latest
EXPOSE 9987/udp 30033 10011
RUN apt-get update \
&& apt-get install -y wget bzip2 \
&& cd /home \
&& wget http://dl.4players.de/ts/releases/3.2.0/teamspeak3-server_linux_amd64-3.2.0.tar.bz2 \
&& bunzip2 teamspeak3-server_linux_amd64-3.2.0.tar.bz2 \
&& tar -xvf teamspeak3-server_linux_amd64-3.2.0.tar
ENV TS3SERVER_LICENSE=accept
WORKDIR /home/teamspeak3-server_linux_amd64
CMD ["sh", "ts3server_minimal_runscript.sh"]
