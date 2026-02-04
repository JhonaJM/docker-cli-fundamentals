# MariaDB

docker pull mariadb:jammy

docker container run \
--name world-db \
-dp 3306:3306 \
--env MARIADB_USER=example-user \
--env MARIADB_PASSWORD=user-password \
--env MARIADB_ROOT_PASSWORD=root-secret-password \
--env MARIADB_DATABASE=world-db \
mariadb:jammy

## Ver contraseña generada
docker logs <container_id>
