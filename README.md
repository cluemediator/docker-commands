# Docker Commands: A Comprehensive List

> Thank you for checking out this project! If you find it useful, please consider giving it a star ⭐. Pull requests are always welcome and greatly appreciated. For more technical updates, follow us on Twitter [@ClueMediator](https://twitter.com/cluemediator).


**Note:** This repository is dedicated to showcasing Docker commands only. If you're interested in more technical content, please visit [Clue Mediator's GitHub profile](https://github.com/cluemediator).


### Table of Contents

- **Process Management**
    - [Show all running docker containers](#show-all-running-docker-containers)
    - [Show all docker containers](#show-all-docker-containers)
    - [Run a container](#run-a-container)
    - [Run a container and connect to it](#run-a-container-and-connect-to-it)
    - [Run a container in the background](#run-a-container-in-the-background)
    - [Stop a container](#stop-a-container)
    - [Kill a container](#kill-a-container)
- **Volumes & Ports**
    - [List volumes](#list-volumes)
    - [Create a volume](#create-a-volume)
    - [Delete a volume](#delete-a-volume)
    - [Show volume metadata](#show-volume-metadata)
    - [Delete all volumes not attached to a container](#delete-all-volumes-not-attached-to-a-container)
    - [Mount a local directory to your container](#mount-a-local-directory-to-your-container)
    - [Copy file or folder from a docker container to host machine](#copy-file-or-folder-from-a-docker-container-to-host-machine)
    - [Copy file or folder from local machine onto a container](#copy-file-or-folder-from-local-machine-onto-a-container)
    - [Map a local port to a docker instance](#map-a-local-port-to-a-docker-instance)
    - [List the ports a docker container is running on](#list-the-ports-a-docker-container-is-running-on)
- **Docker Compose**
    - [Start your docker-compose defined resources in detached mode](#start-your-docker-compose-defined-resources-in-detached-mode)
    - [Stop all docker-compose resources](#stop-all-docker-compose-resources)
    - [Destroy all docker-compose resources](#destroy-all-docker-compose-resources)
    - [Show docker-compose processes](#show-docker-compose-processes)
    - [Show docker-compose logs](#show-docker-compose-logs)
    - [Show docker-compose resource consumption](#show-docker-compose-resource-consumption)
- **Images/Repository**
    - [List available local images](#list-available-local-images)
    - [Search for docker images](#search-for-docker-images)
    - [Pull a docker image](#pull-a-docker-image)
    - [Build an image with a dockerfile](#build-an-image-with-a-dockerfile)
    - [Login to a remote repository](#login-to-a-remote-repository)
    - [Push an image to your remote repository](#push-an-image-to-your-remote-repository)
    - [Remove a local docker image](#remove-a-local-docker-image)
    - [Show metadata for an image](#show-metadata-for-an-image)
    - [Remove all unused docker images](#remove-all-unused-docker-images)
- **Troubleshooting**
    - [Show the logs of a container](#show-the-logs-of-a-container)
    - [Follow/tail the logs of a container](#followtail-the-logs-of-a-container)
    - [Show timestamps on docker logs](#show-timestamps-on-docker-logs)
    - [Show details/metadata of a container](#show-detailsmetadata-of-a-container)
    - [Show a 'top' view of processes running on a container](#show-a-top-view-of-processes-running-on-a-container)
    - [Show a 'top' view of all docker containers](#show-a-top-view-of-all-docker-containers)
    - [Show any files that have changed since startup](#show-any-files-that-have-changed-since-startup)
    - [Connect to an already running container](#connect-to-an-already-running-container)
    - [Execute a command on a container](#execute-a-command-on-a-container)
    - [Show docker system wide information](#show-docker-system-wide-information)
    - [Show docker disk space used](#show-docker-disk-space-used)


## Docker Commands


- ### Process Management

    - #### Show all running docker containers

        ```sh
        docker ps
        ```
        **[⬆ Back to Top](#table-of-contents)**

        
    - #### Show all docker containers

        ```sh
        docker ps -a
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Run a container

        ```sh
        docker run <image>:<tag>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Run a container and connect to it

        ```sh
        docker run -it <image>:<tag>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Run a container in the background

        ```sh
        docker run -d <image>:<tag>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Stop a container

        ```sh
        docker stop <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Kill a container

        ```sh
        docker kill <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

- ### Volumes & Ports

    - #### List volumes

        ```sh
        docker volume ls
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Create a volume

        ```sh
        docker volume create <volume>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Delete a volume

        ```sh
        docker volume rm <volume>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show volume metadata

        ```sh
        docker volume inspect <volume>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Delete all volumes not attached to a container

        ```sh
        docker volume prune
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Mount a local directory to your container

        ```sh
        docker run -v <local_dir>:<container_dir> <image>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Copy file or folder from a docker container to host machine

        ```sh
        docker cp container>:<container_dir> <local_dir>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Copy file or folder from local machine onto a container

        ```sh
        docker cp <local_dir> <container>:<container_dir>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Map a local port to a docker instance

        ```sh
        docker run -d -p 127.0.0.1:<local_port>:<docker_port> <image>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### List the ports a docker container is running on

        ```sh
        docker port <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**


- ### Docker Compose

    
    - #### Start your docker-compose defined resources in detached mode

        ```sh
        docker-compose up -d -f <docker_compose_yaml>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Stop all docker-compose resources

        ```sh
        docker-compose stop
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Destroy all docker-compose resources

        ```sh
        docker-compose down
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show docker-compose processes

        ```sh
        docker-compose ps
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show docker-compose logs

        ```sh
        docker-compose logs
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show docker-compose resource consumption

        ```sh
        docker-compose top
        ```

        **[⬆ Back to Top](#table-of-contents)**



- ### Images/Repository


    - #### List available local images

        ```sh
        docker images
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Search for docker images

        ```sh
        docker search <image>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Pull a docker image

        ```sh
        docker pull <image>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Build an image with a dockerfile

        ```sh
        docker build -t <image>:<tag> <run_directory> -f <dockerfile>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Login to a remote repository

        ```sh
        docker login <repository>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Push an image to your remote repository

        ```sh
        docker push <image>:<tag>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Remove a local docker image

        ```sh
        docker rmi <image>:<tag>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show metadata for an image

        ```sh
        docker inspect <image>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Remove all unused docker images

        ```sh
        docker image prune
        ```

        **[⬆ Back to Top](#table-of-contents)**



- ### Troubleshooting


    - #### Show the logs of a container

        ```sh
        docker logs <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Follow/tail the logs of a container

        ```sh
        docker logs -f <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show timestamps on docker logs

        ```sh
        docker logs -t <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show details/metadata of a container

        ```sh
        docker inspect <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show a 'top' view of processes running on a container

        ```sh
        docker top <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show a 'top' view of all docker containers

        ```sh
        docker stats
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show any files that have changed since startup

        ```sh
        docker diff <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Connect to an already running container

        ```sh
        docker attach <container>
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Execute a command on a container

        ```sh
        docker exec -it <container_id> /bin/bash
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show docker system wide information

        ```sh
        docker system info
        ```

        **[⬆ Back to Top](#table-of-contents)**

    
    - #### Show docker disk space used

        ```sh
        docker system df
        ```

        **[⬆ Back to Top](#table-of-contents)**


---

### **Happy Coding...!! 😊**
