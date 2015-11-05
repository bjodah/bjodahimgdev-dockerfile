# DO NOT EDIT, This Dockerfile is generated from ./tools/10_generate_Dockerfile.sh
FROM bjodah/bjodahimg:latest
MAINTAINER Björn Dahlgren <bjodah@DELETEMEgmail.com>
RUN apt-get update && \
    apt-get --quiet --assume-yes install \
    phantomjs imagemagick && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
