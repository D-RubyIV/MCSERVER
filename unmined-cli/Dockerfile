FROM ubuntu:22.04

RUN apt update && apt install -y wget unzip libglib2.0-0 python3

WORKDIR /app

RUN wget -O unmined-cli.tar.gz "https://unmined.net/download/unmined-cli-linux-x64-dev/?tmstv=1752036379"
RUN tar -xzf unmined-cli.tar.gz
RUN rm unmined-cli.tar.gz
ENTRYPOINT bash -c "./unmined-cli_0.19.49-dev_linux-x64/unmined-cli  && sleep infinity"



