# Icecast docker setup

# Image for container
FROM alpine
MAINTAINER juliusrajala <juliusrajala@gmail.com>

# Installing icecast
RUN apk add --no-cache icecast

# Moving custom icecast-configuration to its place
COPY ./icecast-custom.xml /etc/

# Run icecast
CMD icecast -c /etc/icecast-custom.xml