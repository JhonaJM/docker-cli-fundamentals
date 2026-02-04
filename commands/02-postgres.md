# PostgreSQL Instances

## Instancia con puerto expuesto
docker container run --name postgres-alpha -dp 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword postgres

## Segunda instancia
docker container run \
--name postgres-beta \
-e POSTGRES_PASSWORD=mypass1 \
-dp 5433:5432 \
postgres:14-alpine3.17
