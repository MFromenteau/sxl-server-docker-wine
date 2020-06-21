FROM scottyhardy/docker-wine:latest

ENV DEBIAN_FRONTEND noninteractive

EXPOSE 7777 7777/udp 7778 7778/udp


ENV DISPLAY :0

RUN mkdir /home/skaterxl
WORKDIR /home/skaterxl

COPY server.tar .

RUN tar -xvf server.tar && rm server.tar

VOLUME /maps
WORKDIR /home/skaterxl/server
CMD wineconsole XLMultiplayerServerConsoleApp.exe