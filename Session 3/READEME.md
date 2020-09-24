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

### Run containers

**MySQL**
docker container run -d --name db -e MYSQL_ROOT_PASSWORD=123456 mysql

*show logs*
docker container logs db


**APACHE SERVER**
docker container run -d --name webserver -p 8081:80 httpd

*to test*
CURL localhost:8081


**NGINX**
docker container run -d --name proxy -p 81:80 nginx

*to test*
CURL localhost:81