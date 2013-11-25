docker-dna
==========

DockerDNA Project: Docker + Ansible (local)

Getting Started
----
### Render a DockerDNA-ready base image.  
At this time, only Ubuntu 12.04 is supported.  I'll add others, if interest is apparent.

        git clone https://github.com/wrale/docker-dna.git
        cd ./docker-dna/base
        docker build -t yourname/docker-dna_base:12.04 .

### Render a Docker image based on an existing DockerDNA role.  

        cd ../rabbitmq
        docker build -t yourname/docker-dna_rabbitmq:3.1.5 .

Optionally, you can create your own DockerDNA role using Ansible role syntax.


### Run the container you built:

        docker run -d -t yourname/docker-dna_rabbitmq:3.1.5 ??
