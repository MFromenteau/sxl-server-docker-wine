FROM scottyhardy/docker-wine:latest

ENV DEBIAN_FRONTEND noninteractive

EXPOSE 7777
EXPOSE 7778

ENV DISPLAY :0

RUN mkdir /home/skaterxl
WORKDIR /home/skaterxl

COPY server.tar .

RUN tar -xvf server.tar && rm server.tar

VOLUME /home/skaterxl
WORKDIR /home/skaterxl/server
CMD wineconsole XLMultiplayerServerConsoleApp.exe