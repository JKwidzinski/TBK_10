docker swarm init \
docker stack deploy -c image-gallery.yml image-gallery \
docker-compose -f image-gallery.yml -f update-image-version.yml config > stack.yml 

z jakiegoś powodu w stack.yml trzeba usunąć "" po bokach portów, dokleić version: "3.8" na początku pliku oraz w iotd, przenieść image na góre ustawień tego kontenera 

plik stack.yml w repo jest wersją z poprawionymi wyżej wymienionymi błędami 

docker stack deploy -c stack.yml image-gallery \
docker service ps image-gallery_iotd