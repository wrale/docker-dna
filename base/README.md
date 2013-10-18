# DockerDNA Base 12.04: 
## Ubuntu 12.04 + Ansible

### Run this container:

        docker run -i -t wrale/docker-dna_base:12.04 '/bin/bash'

### Build this container again:

        git clone https://github.com/wrale/docker-dna.git
        cd ./docker-dna/base
        docker build -t yourname/docker-dna_base:12.04 .

### Run the container you built:

        docker run -i -t yourname/docker-dna_base:12.04 '/bin/bash'
