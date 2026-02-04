# Images & Containers Basics

## Descargar imagen
docker pull postgres

## Ejecutar contenedor
docker container run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres

## Listar contenedores
docker ps

## Ver logs
docker logs <container_id>

## Eliminar contenedor
docker rm -f <container_id>
