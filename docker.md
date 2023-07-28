# Docker

Docker is a platform that uses containers to package software and
its depencies into a light and isolated environment

## Key Terms

#### Container:

An isolated process in a machine that can contain an application and all its necessary depenencies. Isolated filesystems provided by an image

#### Image

A template of a container's filesystem. It has everything needed to run the application - all dependencies,configuration, scripts, binaries, etc.  
Also has it's own configuration stored like env vars

#### Environment variables

A default command to run on other metadata

## Getting Started

#### COMMAND

``  
`-`
\_\_

#### See all Docker images

`docker images`  
\_\_

#### Build docker image

`docker build -t <image_name>:<tag> <path_to_docker_file>`  
`-t` name for the image
`-f <path to docker file>` dockerfole path
\_\_

#### See all containers running and not running

`docker ps -a`  
`-a` show all containers  
\_\_

#### Create and run a container

`docker run --name <name> image:version`  
 `-d` detached mode running container in the background  
 `-p` map port of x of the host to port y in the container  
 `--rm` remove container when stopped
\_\_

#### COMMAND

`docker start <container>`  
`-i` interactive
`-`
\_\_

#### Delete container

`docker rm <container_name_or_id>`

---

## Advanced

#### Execute a command into a container

`docker exec -i <container> <command>`  
`-i` interactive. Keep STDIN open even when unattached

## Contributing
