## Docker container for using swagger-tools

### Download and execution

    docker pull mozolo/swagger-tools:latest
    docker run -it --name swgtools -v /home/user/swagger_data_folder:/opt/data mozolo/swagger-tools:latest bash

### Once in the container

First move to the volume folder and then execute swagger-tools.

For example for updating from a Swagger 1.X version to Swagger 2.0.

    cd /opt/data
    swagger-tools convert --yaml ./header.json ./one.json ./two.json ./three.json > ./converted.yaml
    exit
    docker stop swgtools

### For other executions:

    docker start swgtools
    docker exec -it swgtools bash


