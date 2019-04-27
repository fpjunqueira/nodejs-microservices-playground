# Nodejs Microservices Playground

Just playing around microservices with nodejs from scratch and this is the first service.

## RUN

NPM

`npm install && npm start`

Docker

`docker run -d -p 8080:3000 --name node-container -v "$(pwd):/var/www" -w  "/var/www" node npm start`