FROM debian

MAINTAINER Aurele

ENV TS3SERVER_LICENSE=accept
#Variables d'environnement qui permet de reconnaitre la license sinon pas acces au server TeamSpeak 3
WORKDIR /Users/auguitar/Desktop
#Tout ce passera dans le /home/teamspeak
EXPOSE 9987/udp 10011 30033
#Permet au container "d'ecouter" sur des ports du network specific au lancement.
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y wget bzip2 && \
    wget http://dl.4players.de/ts/releases/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2 && \
    tar -xvf teamspeak3-server_linux_amd64-3.8.0.tar.bz2
#1- update tout
#2- upgrade tout
#3- Install un programme qui permet de unzip des doc type bz2
#4- Install un lien d'un serveur teamspeak compresser de teamspeak
#5- Untar ou extraire un fichier type tar qui est le server teamspeak
WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh

# How to build it?
# docker build -t ex01 .

# How to run it?
# docker run --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
