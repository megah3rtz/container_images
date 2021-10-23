FROM lscr.io/linuxserver/code-server
RUN apt-get update -y && apt-get install wget unzip
RUN wget https://releases.hashicorp.com/terraform/1.0.9/terraform_1.0.9_linux_amd64.zip; unzip terraform_1.0.9_linux_amd64.zip; mv terraform /usr/local/bin/

ENTRYPOINT /init
