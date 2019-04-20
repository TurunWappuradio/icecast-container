# Icecast docker setup

# Image for container
FROM alpine
MAINTAINER juliusrajala <juliusrajala@gmail.com>

# Installing icecast
RUN apk add --no-cache icecast

# Moving custom icecast-configuration to its place
COPY ./icecast-custom.xml /etc/
COPY ./intro.mp3 usr/share/icecast/web/
RUN chmod +x usr/share/icecast/web/intro.mp3

# Run icecast
CMD icecast -c /etc/icecast-custom.xml