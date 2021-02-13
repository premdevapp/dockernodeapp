docker build -t <your username>/node-web-app .
docker images
-- name = premdevdis
docker run -d <your username>/node-web-app -p 49160:8080

# Get container ID

docker ps

# Print app output

docker logs <container id>

# Enter the container

$ docker exec -it <container id> /bin/bash

$ docker ps

# Example

ID IMAGE COMMAND ... PORTS
ecce33b30ebf <your username>/node-web-app:latest npm start ... 49160->8080

curl -i localhost:49160
-- sudo apt-get install curl

-- remove
docker system prune

-- stop
docker container stop $(docker container ls -aq)
