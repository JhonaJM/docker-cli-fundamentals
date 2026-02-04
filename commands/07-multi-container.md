# Multi-Container (MariaDB + phpMyAdmin)

En este laboratorio se conectan **múltiples contenedores** usando redes y volúmenes para simular un entorno real de base de datos.

Se practica:

- Redes entre contenedores
- Persistencia con volúmenes
- Variables de entorno
- Comunicación entre servicios

---

## 1️⃣ Crear red

docker network create world-app

---

## 2️⃣ Crear volumen para persistencia

docker volume create world-db

---

## 3️⃣ Levantar MariaDB

docker container run \
--name world-db \
-dp 3306:3306 \
--env MARIADB_USER=example-user \
--env MARIADB_PASSWORD=user-password \
--env MARIADB_ROOT_PASSWORD=root-secret-password \
--env MARIADB_DATABASE=world-db \
--volume world-db:/var/lib/mysql \
--network world-app \
mariadb:jammy

---

## 4️⃣ Levantar phpMyAdmin

docker container run \
--name phpmyadmin \
-d \
-p 8080:80 \
-e PMA_HOST=world-db \
--network world-app \
phpmyadmin:5.2.0-apache

---

## 5️⃣ Acceder

Abrir navegador:

http://localhost:8080

Credenciales:
- servidor: world-db
- usuario: example-user
- password: user-password

---

## Resultado esperado

- phpMyAdmin puede conectarse a MariaDB
- Los datos persisten aunque el contenedor se elimine
- Ambos servicios se comunican por la red Docker

