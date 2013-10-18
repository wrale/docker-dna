
# DockerDNA ZooKeeper 3.4.5.w1: ZooKeeper 3.4.5

## Run this container:

        docker run -d -t wrale/docker-dna_zookeeper:3.4.5.w1 start-foreground

## Build this container again:

        git clone https://github.com/wrale/docker-dna.git
        cd ./docker-dna/zookeeper
        docker build -t yourname/docker-dna_zookeeper:3.4.5.w1 .

## Run the container you built:

        docker run -d -t yourname/docker-dna_zookeeper:3.4.5.w1 start-foreground 

## Determine which container port(s) are listening:

        docker ps
