
# Docker

## Docker-Container erstellen

docker-compose -f docker-compose-hub.yml create


## Startreihenfolge Docker-Container

docker-compose -f docker-compose-hub.yml start activemq cassandra mariadb discovery
docker-compose -f docker-compose-hub.yml start provisioner
docker-compose -f docker-compose-hub.yml start accounting customer identity office portfolio

docker-compose -f docker-compose-hub.yml start fims-web-app


## Container Überblick

docker-compose -f docker-compose-hub.yml ps


## Logging 

docker-attach cassandra
docker-attach discovery
docker logs discovery


## Reset
Um Datenbank zurücksetzen und komplett neu zu starten

docker-compose -f docker-compose-hub.yml stop
docker-compose -f docker-compose-hub.yml rm





