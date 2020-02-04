FROM debian

ENV TS3SERVER_LICENSE=accept

EXPOSE 9987/udp 10011 30033

WORKDIR /home/teamspeak

RUN apt-get update \
	&& apt-get upgrade -y \
	&& apt-get install bzip2 wget -y \
	&& wget http://dl.4players.de/ts/releases/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2
RUN tar xvf teamspeak3-server_linux_amd64-3.8.0.tar.bz2

CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]

# step 1
# docker build -t ex01 .

# step 2
# docker run -it --rm --name ex1 -e TS3SERVER_LICENSE=accept -p 9987:9987/udp -p 10011:10011 -p 30033:30033 teamspeak

# https://www.hostinger.com/tutorials/how-to-make-a-teamspeak-3-server/
# https://support.teamspeakusa.com/index.php?/Knowledgebase/Article/View/44/16/which-ports-does-the-teamspeak-3-server-use
# https://forum.teamspeak.com/threads/137939-Docker-TS3Server-crash-by-reading-licensekey-dat
