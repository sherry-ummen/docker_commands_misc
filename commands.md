# Delete all containers
docker rm --force `docker ps -qa`

# Delete all container images
docker rmi $(docker images -a -q)

# List all docker images
docker images

# Stop all containres
docker stop $(docker ps -a -q)

# Start container in background ( -d ) with name and port
docker run -d --name redisHostPort -p 6379:6379 redis:latest

# Inspect docker 
docker inspect <fiendlyname/containerid>

# Check logs
docker logs <fiendlyname/containerid>

# Mapping driver with option -v hostdir:containerdir
docker run -d --name redisMapped -v /opt/docker/data/redis:/data redis
