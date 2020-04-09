# Docker

## Commands
- `run`: start a container
	- if it doesn't exist locally it will pull from dockerhub the first time 
- `ps`: list containers
- `stop <name>`: stop container, use `ps` to get name
- `rm <name>`: remove a container
- `images`: list images
- `rmi <image name>: remove images
- `attach` `detach`
- logs <container_name>: shows stdout of detached container
## Run - tag
- to run a version of an image `docker run redis:4.0` <image>:<version>

- -i for interactive input
- -t for pseudo terminal
- -d for detached mode; container runs in the background

- docker run -p 80:5000 kodekloud/simple-webapp
	- <docker host port>:<container port>
	- maps the ports to make it accessible
- volume mapping (persist data after removing container ie. mysql)
	- make a copy outside container (in host)
	- docker run -v /opt/datadir:/var/lib/mysql mysql
	- <host>:<container>

## Inspect container
- docker inspect <container_name>
- show additional details that `docker ps` doesn't; in json format
