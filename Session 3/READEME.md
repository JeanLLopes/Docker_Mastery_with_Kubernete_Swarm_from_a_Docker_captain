### DOCKER COMMAND BASIC

-- docker version

-- docker info

-- docker

<br>

### Run a NGINX server

--  docker container run --publish 80:80 nginx

### Remove container with force

-- docker container rm -f {CONTAINER ID}

### List all life container

-- docker container ls -a
-- docker container ps


### List running processis in specific container

-- docker top {CONTAINER ID}