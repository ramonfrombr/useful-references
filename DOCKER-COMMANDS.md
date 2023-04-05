## Build a container image

`docker build -t IMAGE_NAME DIRECTORY`

`docker container ls`

`docker compose up`

`docker compose up -d`

`docker compose down`

`docker container ls`

`docker images`

`sudo docker rmi $(sudo docker images -q)`

`docker ps -a`

`docker rm NAME`

`docker stop NAME`

`docker volume ls`

Binding local files to files in container for faster development process

`docker run -v pathtofolderonlocation:pathtofolderoncontainer -p 3000:3000 -d --name node-app node-app-image`

``
