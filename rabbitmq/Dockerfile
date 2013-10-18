# docker-dna/rabbitmq/Dockerfile
#
# VERSION    3.1.5.w1
#
FROM wrale/docker-dna_base:12.04
MAINTAINER Joshua Dotson, josh@wrale.com

# Update distribution
RUN apt-get update \
      && apt-get upgrade -y \
      && apt-get clean

# Add files
ADD . ./DockerDNA

# Install RabbitMQ
RUN ( echo '[docker-dna_rabbitmq]' && \
      echo 'localhost' \
    ) > /etc/ansible/hosts \
      && ansible-playbook ./DockerDNA/dna.yml --connection=local \
      && apt-get clean      

# Expose RabbitMQ
EXPOSE 4369 5672 15672 35197
#ENTRYPOINT [""]
#CMD ["--help"]
