# docker cheat sheet

## Images

`docker images`

`docker pull ubuntu`

`docker rmi ubuntu`

## Containers

`docker ps -a`

`docker run -it ubuntu --name ubuntu-container`

`docker start ubutu-container`

`docker exec -it ubutu-container bash`

`docker start -a -i ubutu-container`

`docker stop ubutu-container`

`docker rm ubutu-container`

`docker rm $(docker ps -a | awk {'print $1'})`

`docker container prune`

**Deteched**

`docker run -d dockersamples/static-site`

`docker stop -t 0 distracted_almeida`

**Binding Ports**

`docker run -d -P dockersamples/static-site`

`docker run -d -p 12345:80 dockersamples/static-site`

`docker port eager_napier`

**Environment**

`docker run -d -P -e AUTHOR='Felipe' dockersamples/static-site`

`docker stop -t 0 $(docker ps -q)`

**Volumes**

`docker run --name ubuntu-container -v "/var/www" ubuntu`

`docker inspect ubuntu-container`

`docker run -it --name ubuntu-container -v "$(pwd):/var/www" ubuntu`

**Running a project into a node container**

-w: working directory

`docker run -d -p 8080:3000 --name node-container -v "$(pwd):/var/www" -w  "/var/www" node npm start`
 