FROM debian
WORKDIR teamspeak3-server_linux_amd64
EXPOSE 10011 
EXPOSE 30033
EXPOSE 9987/udp
ENV    TS3SERVER_LICENSE   "accept"
ENV    TS3SERVER_VERSION   "3.5.0"
RUN apt-get update -y 
RUN apt-get full-upgrade -y
RUN apt-get install wget bzip2 -y
RUN wget http://dl.4players.de/ts/releases/3.5.0/teamspeak3-server_linux_amd64-3.5.0.tar.bz2 
RUN tar -xvf teamspeak3-server_linux_amd64-3.5.0.tar.bz2


CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]

# docker build -t teamspeak .
# docker run -it --rm -p 30033:30033 -p 9987:9987/udp -p 10011:10011 teamspeak

# first command that compiles the docker file into a docker image.
#second command lets you run the docker image with the second command.
