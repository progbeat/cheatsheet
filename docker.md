Action | Command
---|---|
Start an interactive bash session | `docker run -it ubuntu bash`
Kill all runnning docker containers |	`docker kill $(docker ps -q)`
Delete dangling Docker images |	`docker rmi $(docker images -q -f dangling=true)`
Remove all stopped containers |	`docker rm $(docker ps -a -q)`
Start interactive bash session into the container | `docker exec -it CONTAINER_NAME bash`
[List containers](https://docs.docker.com/engine/reference/commandline/container_ls/) | `docker container ls`
Add a secret | `printf "This is a secret" \| docker secret create my_secret_data -`
Get IP address of container | `docker inspect -f "{{ .NetworkSettings.IPAddress }}" CONTAINER_NAME`
Save container state into a new image `IMAGE_NAME` | `docker commit CONTAINER_ID IMAGE_NAME`
Print the container's logs starting from the last 100 lines | `docker logs -f -n 100 CONTAINER_ID`
