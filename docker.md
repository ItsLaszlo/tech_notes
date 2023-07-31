# Docker

Docker is a platform that uses containers to package software and
its depencies into a light and isolated environment

## Key Terms

#### Container:

An isolated process in a machine that can contain an application and all its necessary depenencies. Isolated filesystems provided by an image  
\*\*\*\*\*\*\*\*\*\*

#### Context:

A specific environment where Docker operates and performs actions. Similar to a BE(Boot Environment) has the exact rules, settings, and configurations/conditions needed by the app. _ The configuration and settings for Docker to interact with different conatainer env_ Examples: local Docker install, remote Docker host, or a cloud-based container service like AWS ECS or kubernetes.  
\*\*\*\*\*\*\*\*\*\*

#### Volumes:

Map specific filesystem path on local machine to the container for persistent data  
_Named Volumes:_ Bucket of data. Docker maintains the physical location on the disk. End user names only needs to remember the name of the volume
\*\*\*\*\*\*\*\*\*\*

#### Image:

A template of a container's filesystem. It has everything needed to run the application - all dependencies,configuration, scripts, binaries, etc.  
Also has it's own configuration stored like env vars
\*\*\*\*\*\*\*\*\*\*

#### Environment variables:

A default command to run on other metadata  
\*\*\*\*\*\*\*\*\*\*

#### Tags:

Giving it a unique name and version to be easily identifiable and allows others to pull specific version
\*\*\*\*\*\*\*\*\*\*

---

## Getting Started

#### COMMAND

``  
`-`
\*\*\*\*\*\*\*\*\*\*

#### See all Docker images

`docker images`  
\*\*\*\*\*\*\*\*\*\*

#### Build docker image

`docker build -t <image_name>:<tag> <path_to_docker_file>`  
`-t` name for the image  
`-f <path to docker file>`  
\*\*\*\*\*\*\*\*\*\*

#### See all containers running and not running

`docker ps -a`  
`-a` show all containers  
\*\*\*\*\*\*\*\*\*\*

#### Create and run a container

`docker run --name <name> <image>:<version> <optional_corresponding_interprt> <optional_cmnd>`

`-d` detached mode running container in the background  
 `-p` map port of x of the host to port y in the container  
 `--rm` remove container when stopped  
 `-v <volume_name>:<cntner_pth>` volume to mount to container
--
`<username>/<repo_name>` Can include the user and the repo of that user you want to pull an image from instead of `<image>:<version>`  
`<optional_interprt> <optional_cmnd>` command to be ran in the container
example: `bash -c "echo Hello!"` | `sh -c "echo Hello!` | `python /path/to/your/project.py`  
\*\*\*\*\*\*\*\*\*\*

#### Rename a container

`docker rename <og_name> <new_name>`  
` `  
\*\*\*\*\*\*\*\*\*\*

#### Start Docker container

`docker start <container>`  
`-i` interactive  
\*\*\*\*\*\*\*\*\*\*

#### Stop Docker container

`docker stop <container>`  
` `  
\*\*\*\*\*\*\*\*\*\*

#### Change the environment where Docker operates.

`docker context create ecs myecscontext`  
` `  
\*\*\*\*\*\*\*\*\*\*

#### Delete the container

`docker rm <container_name_or_id>`  
`-f` forcefully stop the container if running and then delete it

---

## Advanced

#### Volume

`docker volume <action>`  
`create <name_volume>`  
`inspect` see info of volume  
`ls` see list of volumes  
\*\*\*\*\*\*\*\*\*\*

#### Execute a command into a container

`docker exec <container> <command>`  
`-i` interactive. Keep STDIN open even when unattached  
`-t` Allocate a pseudo-TTY(emulation of a physical terminal)
_Example:_  
`docker exec -it 56a714cded3b /bin/bash` open an interactive session with a pseudo-TTY pointing to the shell intrepeter /bin/bash  
`docker exec 56a714cded3b cat /data.txt`  
\*\*\*\*\*\*\*\*\*\*

#### Create a tag for an existing docker image.

`docker tag <image name>:<optional_tag> <YOUR-USER-NAME>/<repo name>`  
\*\*\*\*\*\*\*\*\*\*

#### Push docker image into Docker hub repo

`docker push <username>/<image_name>:<optinal_tag>`

\*\*\*\*\*\*\*\*\*\*

## Configs

#### Docker Image file

A docker file defines the configuration and instructions for building a docker container image  
The file is named _Dockerfile_

---

## Sharing an App

1. Create an image
2. Test image and create a container
3. Upload image to Docker Hub  
   a. Create repo
   b. Tag image  
   c. Push image
