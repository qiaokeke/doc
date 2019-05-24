FROM golang:1.12

RUN apt-get update && apt-get install -y \
        openssl \
        net-tools \
        git \
        locales \
        sudo \
        dumb-init \
        vim \
        curl \
        wget

# We unfortunately cannot use update-locale because docker will not use the env variables
# configured in /etc/default/locale so we need to set it manually.

# We create first instead of just using WORKDIR as when WORKDIR creates, the user is root.

RUN wget https://github.com/cdr/code-server/releases/download/1.1119-vsc1.33.1/code-server1.1119-vsc1.33.1-linux-x64.tar.gz
RUN tar zxvf code-server1.1119-vsc1.33.1-linux-x64.tar.gz
RUN mv code-server1.1119-vsc1.33.1-linux-x64/code-server /usr/local/bin/
# This assures we have a volume mounted even if the user forgot to do bind mount.
# So that they do not lose their data if they delete the container.
VOLUME [ "/go/src" ]

WORKDIR [ "/go/src" ]

EXPOSE 8443

CMD ["code-server","--allow-http","--no-auth"]
