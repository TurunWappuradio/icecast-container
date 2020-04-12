# Icecast docker setup

# Image for container
FROM debian:buster

# install gcc and make
RUN apt-get update -qq && \
    apt-get install -y -qq gcc make

# install packages needed for building icecast
RUN apt-get install -y -qq libxslt1-dev libvorbis-dev

# install wget
RUN apt-get -y -qq install wget

# Installing icecast
RUN mkdir -p /usr/src/icecast && \
    cd /usr/src/icecast && \
    wget http://downloads.xiph.org/releases/icecast/icecast-2.4.0.tar.gz && \
    tar -xf icecast-2.4.0.tar.gz && \
    cd icecast-2.4.0 && \
    ./configure -prefix=/opt/icecast/2.4.0 && \
    make && make install

# Moving custom icecast-configuration to its place
COPY ./icecast.xml /etc/
COPY ./intro.mp3 usr/share/icecast/web/
RUN chmod +x usr/share/icecast/web/intro.mp3

# Run icecast
CMD icecast -c /etc/icecast.xml
