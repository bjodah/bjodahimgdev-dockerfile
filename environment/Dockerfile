# DO NOT EDIT, This Dockerfile is generated from ./tools/10_generate_Dockerfile.sh
FROM bjodah/bjodahimg:latest
MAINTAINER Björn Dahlgren <bjodah@DELETEMEgmail.com>
RUN apt-get update && \
    apt-get --quiet --assume-yes install \
    flex bison gperf ruby perl \
    libsqlite3-dev libfontconfig1-dev libssl-dev libjpeg-dev libx11-dev libxext-dev && \
    git clone git://github.com/ariya/phantomjs.git && \
    cd phantomjs && \
    git checkout 2.0 && \
    ./build.sh && \
    mv bin/phantom /usr/local/bin && \
    cd .. && \
    rm -r phantomjs && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
