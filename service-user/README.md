# User Service

CRUD user domain

## RUN

**NPM**

`npm install && npm start`

**Docker RUN**

`docker run -d -p 8081:3000 --name user-service -v "$(pwd):/var/www" -w  "/var/www" node npm start`