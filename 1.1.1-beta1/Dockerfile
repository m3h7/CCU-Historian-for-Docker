FROM openjdk:8-jre
MAINTAINER Thomas Zahari <thomas.zahari@gmail.com>

ADD ./install.sh /tmp/
ADD ./start.sh /tmp/

WORKDIR /tmp

RUN bash -el /tmp/install.sh https://github.com/mdzio/ccu-historian/releases/download/1.1.1beta1/ccu-historian-1.1.1beta1-bin.zip

ENV CONFIG_TYPE=CCU2

EXPOSE 80 2098 2099

VOLUME ["/database","/opt/ccu-historian/config"]

ENTRYPOINT ["/opt/ccu-historian/start.sh"]
