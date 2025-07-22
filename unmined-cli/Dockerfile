FROM ubuntu:22.04

RUN apt update && apt install -y wget unzip libglib2.0-0 python3

WORKDIR /app

RUN wget -O unmined-cli.tar.gz "https://unmined.net/download/unmined-cli-linux-x64-dev/?tmstv=1752036379" && \
    tar -xzf unmined-cli.tar.gz && \
    rm unmined-cli.tar.gz

ENTRYPOINT bash -c 'mkdir -p /tmp/minimap; while true; do \
  echo "[uNmINeD] Starting render at $(date)"; \
  ./unmined-cli_0.19.49-dev_linux-x64/unmined-cli web render \
    --world="/data/worlds/Bedrock level" \
    --output="/tmp/minimap"; \
  echo "[uNmINeD] Copying to /minimap..."; \
  rm -rf /minimap/* && cp -r /tmp/minimap/* /minimap/; \
  echo "[uNmINeD] Waiting 10 seconds..."; \
  sleep 10; \
done'
