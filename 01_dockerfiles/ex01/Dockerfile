# BYOTSS

FROM debian
LABEL Description="Launches a TeamSpeak server from within debian."
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "wget"]
RUN ["apt-get", "install", "-y", "bzip2"]
RUN ["wget", "http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2"]
RUN ["tar", "-xjvf", "teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2"]
EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011
EXPOSE 41144
ENTRYPOINT ["teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]
