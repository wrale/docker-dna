# docker-dna/base/Dockerfile
#
# NAME       wrale/docker-dna_base
# VERSION    12.04.w2
#
FROM ubuntu:12.04
MAINTAINER Joshua Dotson, josh@wrale.com

# Update distribution
RUN ( echo 'deb http://archive.ubuntu.com/ubuntu precise main' && \
      echo 'deb http://archive.ubuntu.com/ubuntu precise-updates main' && \
      echo 'deb http://security.ubuntu.com/ubuntu precise-security main' && \
      echo 'deb http://archive.ubuntu.com/ubuntu precise universe' && \
      echo 'deb http://archive.ubuntu.com/ubuntu precise-updates universe' \
    ) > /etc/apt/sources.list \
      && apt-mark hold upstart \
      && apt-mark hold initscripts \
      && dpkg-divert --local --rename --add /sbin/initctl \
      && ln -s /bin/true /sbin/initctl \
      && apt-get update \
      && apt-get upgrade -y \
      && apt-get clean

# Install base dependencies (Ubuntu <= 12.04)
RUN apt-get install curl python-software-properties -y \
      && add-apt-repository ppa:rquillo/ansible -y \
      && apt-get update \
      && apt-get install ansible -y \
      && apt-get clean
