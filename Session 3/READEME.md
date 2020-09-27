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

_____

<br>

**LOGS ON CONTAINER**

> docker container top
 - process list in one container

<br>

> dokcer container inspect
 - details of one container config

<br>

> docekr container status
  -  performance status of all containers

<br>

> docker container stats

-   listthe process on live of containers


<br>

**SHELL INSIDE DOCKER CONTAINER**
<br>
> docker container run -it [CONTAINER-NAME] bash
- start new container with shell enable
<br><br>
> docker container exec -it [CONTAINER-NAME] bash
- run adicional command in existing container
<br><br>

**DOCKER NETWORK**
<br>
> docker container port [CONTAINER-NAME]
- show port of container
<br>
> docker container inspect --format "{{ >NetworkSettings.IPAddress}}" [CONTAINER-NAME
- show real IP of container
- ["--format" reference](https://docs.docker.com/config/formatting/)
<br>
> docker network ls 

- When you see all networks in docker container **BRIDGE is the default netwotk** is crete when you start a any container and is shared for all container by default
<br>
> docker network inspect
- spect a network
<br>
> docker network create --drive [NAME-OF-NETWORK]
<br>

> docker network connect [ID-CONTAINER] [ID-CONTAINER] [ID-CONTAINER] ...
- connect any containers in a network
<br>
> docker network disconnect  [ID-CONTAINER] [ID-CONTAINER] [ID-CONTAINER] .
 
- disconnect any conatiners in a network
<br>
<br>
 
How connect any networks, to test a communication try this command.
<br>
> docker container exec -it [CONTAINER_NAME] ping [NEW_CONTAINER_NAME]
 - if ping return success.. its OKay

