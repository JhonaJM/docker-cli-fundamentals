# Volumes

## Crear volumen
docker volume create world-db

## Usar volumen para persistencia
docker container run \
--name world-db \
-dp 3306:3306 \
--volume world-db:/var/lib/mysql \
mariadb:jammy
