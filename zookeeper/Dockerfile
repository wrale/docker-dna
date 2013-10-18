# docker-dna/zookeeper/Dockerfile
#
# VERSION    3.4.5.w1
#
FROM wrale/docker-dna_base:12.04
MAINTAINER Joshua Dotson, josh@wrale.com

# Update distribution
RUN apt-get update \
      && apt-get upgrade -y \
      && apt-get clean

# Add files
ADD . ./DockerDNA

# Install ZooKeeper
RUN ( echo '[docker-dna_zookeeper]' && \
      echo 'localhost' \
    ) > /etc/ansible/hosts \
      && ansible-playbook ./DockerDNA/dna.yml --connection=local \
      && apt-get clean      

# Expose ZooKeeper
EXPOSE 2181 2888 3888
ENTRYPOINT ["/usr/lib/zookeeper/bin/zkServer.sh"]
CMD ["--help"]
