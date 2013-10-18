
# DockerDNA Base 12.04.w1: 
## Ubuntu 12.04

### Run this container:

        docker run -i -t wrale/docker-dna_base:12.04.w1 '/bin/bash'

### Build this container again:

        git clone https://github.com/wrale/docker-dna.git
        cd ./docker-dna/base
        docker build -t yourname/docker-dna_base:12.04.w1 .

### Run the container you built:

        docker run -i -t yourname/docker-dna_base:12.04.w1 '/bin/bash'
