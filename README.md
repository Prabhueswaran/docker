# docker
docker

# To install Docker 

From this link - https://get.docker.com/

`curl -fsSL https://get.docker.com -o get-docker.sh`

`sh get-docker.sh`

# To pull the docker image from docker Hub 

`docker pull nginx`

# To run the docker container 

`docker container run -p 80:80 --name my_container nginx:latest`

### Run the container with ditached mode

`docker container run -d -p 80:80 --name my_container nginx:latest`

# To check the running Container 

`docker ps`

# To Stop running container

`docker stop container id`

# To check the stopped container

 `docker ps -a`
 
 # To kill the stopped container 
 
 `docker rm container_id`
