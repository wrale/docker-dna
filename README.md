docker-dna
==========

DockerDNA Project: Docker + Ansible (local)

Getting Started
----

### Render a DockerDNA-ready base image.  
Only Ubuntu 12.04 is supported at this time.  I'll add others if interest is apparent.

        git clone https://github.com/wrale/docker-dna.git
        cd ./docker-dna/base
        docker build -t yourname/docker-dna_base:12.04 .

### Render a Docker image based on an existing DockerDNA role.  

        cd ../rabbitmq
        docker build -t yourname/docker-dna_rabbitmq:3.1.5 .

### Run a container using the image you just built:

        docker run -d -t yourname/docker-dna_rabbitmq:3.1.5 ??

### Create your own DockerDNA roles using [Ansible Best Practices](http://www.ansibleworks.com/docs/playbooks_best_practices.html).

Take a look at the zookeeper/ and rabbitmq/ directories for reference.
