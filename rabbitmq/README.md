
# DockerDNA RabbitMQ 3.1.5:
## RabbitMQ 3.1.5

### Run this container:

        docker run -d -t wrale/docker-dna_rabbitmq:3.1.5 ??

### Build this container again:

        git clone https://github.com/wrale/docker-dna.git
        cd ./docker-dna/rabbitmq
        docker build -t yourname/docker-dna_rabbitmq:3.1.5 .

### Run the container you built:

        docker run -d -t yourname/docker-dna_rabbitmq:3.1.5 ??

### Determine which container port(s) are listening:

        docker ps
