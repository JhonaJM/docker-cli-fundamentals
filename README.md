# Docker CLI Fundamentals

Repositorio de laboratorio donde practico **Docker desde la línea de comandos (CLI)** aprendiendo los conceptos básicos antes de usar Dockerfile o Docker Compose.

El objetivo es entender cómo funcionan los contenedores internamente ejecutando todo manualmente.

Este proyecto forma parte de mi ruta de aprendizaje DevOps.

---

## 🎯 Objetivos de aprendizaje

En este laboratorio practiqué:

* docker pull
* docker run
* docker rm
* docker ps
* publicación de puertos
* variables de entorno
* logs
* modo detached
* terminal interactiva
* volúmenes (anónimos y nombrados)
* persistencia de datos
* redes entre contenedores
* aplicaciones multi-contenedor
* inspección del file system dentro del contenedor

---

## 📚 Laboratorios incluidos

### 1️⃣ Contenedores básicos

* Ejecutar imágenes
* Exponer puertos
* Variables de entorno
* Logs

### 2️⃣ PostgreSQL

* Crear múltiples instancias
* Mapear puertos distintos

### 3️⃣ MariaDB

* Configuración por variables de entorno
* Creación automática de base de datos
* Conexión desde cliente externo

### 4️⃣ Volúmenes

* Persistencia de datos
* docker volume create
* evitar pérdida de información al eliminar contenedores

### 5️⃣ Redes

* Comunicación entre contenedores
* docker network create
* docker network connect

### 6️⃣ phpMyAdmin + MariaDB (multi-contenedor)

* Administración visual de base de datos
* Conexión entre servicios mediante redes

---

## 📂 Estructura

```
commands/   → comandos organizados por tema
assets/     → archivos auxiliares
```

---

## 🧠 Resultado de aprendizaje

Después de este laboratorio ya puedo:

✅ Administrar contenedores desde la CLI

✅ Crear entornos de bases de datos rápidamente

✅ Persistir datos con volúmenes

✅ Conectar múltiples servicios por redes

✅ Debuggear usando logs y exec

✅ Entender cómo funciona Docker sin depender de GUIs

