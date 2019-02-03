# Icecast docker setup

# Image for container
FROM alpine
MAINTAINER juliusrajala <juliusrajala@gmail.com>

# Installing icecast
RUN apk add --no-cache icecast

# Moving custom icecast-configuration to its place
ADD ./icecast-custom.xml /etc/icecast.xml

# Run icecast
CMD icecast -c /etc/icecast.xml