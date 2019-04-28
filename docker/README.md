# docker cheat sheet

## Images

`docker images`

`docker pull ubuntu`

`docker rmi ubuntu`

## Containers

`docker ps -a`

`docker run -it ubuntu --name ubuntu-container`

`docker rm ubutu-container`

`docker rm $(docker ps -a | awk {'print $1'})`

`docker container prune`

**Deteched**

`docker run -d dockersamples/static-site`

`docker exec -it ubutu-container bash`

`docker start -a -i ubutu-container`

`docker stop -t 0 ubutu-container`

`docker stop -t 0 $(docker ps -q)`

**Binding Ports**

`docker run -d -P dockersamples/static-site`

`docker run -d -p 12345:80 dockersamples/static-site`

`docker port eager_napier`

**Environment**

`docker run -d -P -e AUTHOR='Felipe' dockersamples/static-site`

**Volumes**

`docker run --name ubuntu-container -v "/var/www" ubuntu`

`docker inspect ubuntu-container`

`docker run -it --name ubuntu-container -v "$(pwd):/var/www" ubuntu`

**Running a project into a node container with volumes**

-w: working directory

`docker run -d -p 8080:3000 --name node-container -v "$(pwd):/var/www" -w  "/var/www" node npm start`

**Dockerfile Build && RUN**

`docker build -f Dockerfile -t fjunqueira/service-1 .`

`docker run -d -p 8080:3000 fjunqueira/service-1`

**Docker HUB**

`docker login`

`docker push fjunqueira/service-1`

`docker pull fjunqueira/service-1`

**Network**

`docker network create --driver bridge my-network`

`docker network list`

`docker run -p 8080:3000 --name service-node-1 --network my-network fjunqueira/service-1`

`docker run -p 8081:3000 --name service-node-2 --network my-network fjunqueira/service-1`

`docker exec -it service-node-1 bash`

`ping service-node-2`


**Docker Compose**

`docker-compose build`

`docker-compose up -d --scale project-service=3`

`docker-compose ps`

`docker-compose down`

`docker exec -it user-service ping project-service`

`docker-compose restart`