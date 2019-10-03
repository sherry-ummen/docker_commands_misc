# Delete all containers
docker rm --force `docker ps -qa`

# Delete all container images
docker rmi $(docker images -a -q)

# List all docker images
docker images


