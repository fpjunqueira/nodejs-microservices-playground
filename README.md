# Nodejs Microservices Playground

Just playing around microservices with nodejs from scratch and this is the first service.

## RUN

**NPM**

`npm install && npm start`

**Docker RUN**

`docker run -d -p 8080:3000 --name node-container -v "$(pwd):/var/www" -w  "/var/www" node npm start`

**Docker Build && RUN**

`docker build -f Dockerfile -t fpjunqueira/service-1 .`

`docker run -d -p 8080:3000 fpjunqueira/service-1`