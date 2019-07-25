FROM openjdk:8-jre
MAINTAINER m3h7

ADD ./install.sh /tmp/
ADD ./start.sh /tmp/

WORKDIR /tmp

RUN bash -el /tmp/install.sh https://github.com/mdzio/ccu-historian/releases/download/2.1.0/ccu-historian-2.1.0-bin.zip

ENV CONFIG_TYPE=CCU3

EXPOSE 80 2098 2099

VOLUME ["/database","/opt/ccu-historian/config"]

ENTRYPOINT ["/opt/ccu-historian/start.sh"]
