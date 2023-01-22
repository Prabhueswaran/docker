# Docker

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

`docker stop container_id`

# To check the stopped container

 `docker ps -a`
 
 # To kill the stopped container 
 
 `docker rm container_id`
 
 
 # To run custom docker container 
 
 **Step1:** Create own source code 
 
 `echo "Devops class" > index.html`
 
 **Step2:** Create Dockerfile

 `vim Dockerfile`
 
 `FROM nginx:latest
  COPY index.html /usr/share/nginx/html/
`

 Save the file
 
 **Step3:** Build the Docker image
 
 `docker build -f Dockerfile -t my_custom_image .`
 
 **Step4:** check the custom image which we created
 
 `docker image ls`
 
 **Step5:** Run the docker container with custom image
 
 `docker container run -d -p 82:80 --name my_custom_container my_custom_image`
 
 **Step6:** check the running container 
 
 `docker ps`
 
 Verify the custom application with IP and port number on browser
 
 # Docker Volume
 
 To mount host volume to container volume
 
 `docker container run -d -p 81:80 -v /home/ubuntu/web_data:/usr/share/nginx/html/ --name my_custom_container nginx`
 
 
 
