Action | Command
---|---|
Start an interactive bash session | `docker run -it ubuntu bash`
Kill all runnning docker containers |	`docker kill $(docker ps -q)`
Delete dangling Docker images |	`docker rmi $(docker images -q -f dangling=true)`
Remove all stopped containers |	`docker rm $(docker ps -a -q)`
[List containers](https://docs.docker.com/engine/reference/commandline/container_ls/) | `docker container ls`
Add a secret | `printf "This is a secret" \| docker secret create my_secret_data -`
