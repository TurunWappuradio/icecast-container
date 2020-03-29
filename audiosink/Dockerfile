# Icecast docker setup

# Image for container
FROM alpine

# Installing icecast
RUN apk add --no-cache icecast

# Moving custom icecast-configuration to its place
COPY ./icecast.xml /etc/
COPY ./intro.mp3 usr/share/icecast/web/
RUN chmod +x usr/share/icecast/web/intro.mp3

# Run icecast
CMD icecast -c /etc/icecast.xml
