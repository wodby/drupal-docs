# Make commands

We provide [`docker.mk`](https://github.com/wodby/docker4drupal/blob/5.x/docker.mk) file that contains commands to simplify the work with your local environment. Once you rename it to `Makefile` or include it to your own Makefile, you can run `make [COMMAND]` to execute the following commands:

```
Usage: make COMMAND

Commands:
    up      Start up all container from the current docker-compose.yml 
    stop    Stop all containers for the current docker-compose.yml (docker-compose stop) 
    down    Same as stop
    prune   Stop and remove containers, networks, images, and volumes (docker-compose down)
    ps      List container for the current project (docker ps with filter by name)
    shell   Enter PHP container as default user (docker exec -ti $CID sh)
```
