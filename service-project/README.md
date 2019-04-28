# Project Service

CRUD project domain

## RUN

**NPM**

`npm install && npm start`

**Docker RUN**

`docker run -d -p 8080:3000 --name project-service -v "$(pwd):/var/www" -w  "/var/www" node npm start`