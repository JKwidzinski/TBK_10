docker image build -t tbk-10-1 . \
docker swarm init \
docker service create --detach --replicas 1 tbk-10-1 \
docker ps -a