# Icecast docker setup

# Image for container
FROM alpine

# Installing icecast
RUN apk add --no-cache icecast

# Moving custom icecast-configuration to its place
COPY ./icecast.xml /etc/

# Run icecast
CMD icecast -c /etc/icecast.xml
