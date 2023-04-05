## Build a container image

`docker build -t IMAGE_NAME DOCKERFILE_DIRECTORY`

`docker container ls`

`docker compose up`

## Runs docker container in detach mode

`docker compose up -d`

## Rebuilds the image and runs the docker container

`docker compose up -d --build`

## Combining docker compose files for running container

`docker compose -f docker-compose.yml -f docker-compose.dev.yml up -d`

## Deletes container ran by Docker Compose

`docker compose down`

## Deletes container and volumes
 
`docker compose down -v`

`docker container ls`

`docker images`

`sudo docker rmi $(sudo docker images -q)`

`docker ps -a`

`docker rm NAME`

`docker stop NAME`

`docker volume ls`

## Binding local files to files in container for faster development process

`docker run -v "$(pwd)":/app -p 3000:3000 -d --name node-app node-app-image`

## Prevents bind module from deleting node_modules

`docker run -v "$(pwd)":/app -v /app/node_modules -p 3000:3000 -d --name node-app node-app-image-dev`

## Read only binding local (prevents container from creating files in the source folder)

`docker run -v "$(pwd)":/app:ro -v /app/node_modules -p 3000:3000 -d --name node-app node-app-image-dev`

## Defining environment variable on runtime when running container

`docker run -v "$(pwd)":/app:ro -v /app/node_modules --env PORT=4000 -p 3000:4000 -d --name node-app node-app-image-dev`

## Runing container with .env file for environment variables

`docker run -v "$(pwd)":/app:ro -v /app/node_modules --env-file ./.env -p 3000:6000 -d --name node-app node-app-image-dev`

## Run bash to access files in container

`docker exec -it node-app bash`

## Non default dockerfile for development

`docker build -f Dockerfile.dev -t devimage .`

## Deletes a specific volume

`docker volume rm VOLUME_NAME`

## Deletes all unused volumes

`docker volume prune`

## Delete a docker container along with its volumes

`docker rm node-app -fv`
