
FROM lscr.io/linuxserver/code-server:latest
ARG tfversion=1.2.7
LABEL org.opencontainers.image.source https://github.com/megah3rtz/container_images
RUN apt-get update -y && \
  apt-get install wget unzip python3-pip -y && \
  pip3 install azure-cli ansible && \
  apt-get clean && \
  rm -rf \
    /tmp/* \
    /var/lib/apt/lists/* \
    /var/tmp/*
RUN wget https://releases.hashicorp.com/terraform/${tfversion}/terraform_${tfversion}_linux_amd64.zip && \
  unzip terraform_${tfversion}_linux_amd64.zip && \
  rm -rf terraform_${tfversion}_linux_amd64.zip && \
  mv terraform /usr/local/bin/

ENTRYPOINT /init
