FROM debian
RUN    apt-get update && apt-get upgrade -y && apt-get install \
    --no-install-recommends \
    build-essential \
    ca-certificates \
    git \
    golang-go \
    sqlite \
    libsqlite3-dev \
    openssh-server -y && \
    mkdir -p /usr/lib/go-1.7/src/github.com/gogs && \
    cd /usr/lib/go-1.7/src/github.com/gogs && \
    git clone --recurse-submodules -b develop https://github.com/gogs/gogs.git && \
    cd gogs && \
    go build -v -tags 'sqlite'
ENV USER="root"
WORKDIR /usr/lib/go-1.7/src/github.com/gogs/gogs
EXPOSE 3000 22
USER root
CMD ["./gogs", "web"]
