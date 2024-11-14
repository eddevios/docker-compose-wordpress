# ENGLISH 

# Docker Configuration for WordPress with MariaDB and PhpMyAdmin

This repository contains a `docker-compose.yml` file to set up a WordPress development environment with MariaDB as the database server and PhpMyAdmin for database management.

## Description

This configuration includes:
* **MariaDB**: as the database server.
* **PhpMyAdmin**: to manage the MariaDB database through a web interface.
* **WordPress**: as the main application.

### Prerequisites

Make sure you have installed:

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)

### Installation

1. **Clone this repository**:
   ```bash
   git clone https://github.com/tu-usuario/docker-compose-wordpress.git
   cd docker-compose-wordpress
2. **Run Docker Compose**: In the repository folder, run:
   ```bash
   docker-compose up -d
This command will download the necessary images (if not already downloaded) and start the containers in detached mode.

## Services and Ports

* **WordPress**: http://localhost:8083
* **PhpMyAdmin**: http://localhost:8082
* **User**: eddevios
* **Password**: 123456

## Environment Configuration

The `docker-compose.yml` file configures the following:

* **MariaDB Database**:
	+ Database name: db_eddevios
	+ User: eddevios
	+ Password: 123456
	+ Root password: root123
* **WordPress Configuration**:
	+ WordPress connects to the MariaDB database container using the above credentials.

## Volumes

This configuration includes volumes to persist data:

* `db_data`: stores MariaDB database data
* `wordpress_data`: stores WordPress files

## Stopping Containers

To stop the containers, run:
  ```bash
  docker-compose down
```
# Troubleshooting
Database connection errors: ensure that the PMA_HOST, WORDPRESS_DB_HOST, and other environment variables in docker-compose.yml are configured correctly.
Port conflicts: change the port mappings in docker-compose.yml if these ports are already in use.

# License
## This project is licensed under the GNU General Public License v3.0.

# SPANISH 
# Configuración de Docker para WordPress con MariaDB y PhpMyAdmin

Este repositorio contiene un archivo `docker-compose.yml` para configurar un entorno de desarrollo de WordPress con MariaDB como servidor de base de datos y PhpMyAdmin para la gestión de la base de datos.

## Descripción

Esta configuración incluye:
* **MariaDB**: como servidor de base de datos.
* **PhpMyAdmin**: para gestionar la base de datos de MariaDB a través de una interfaz web.
* **WordPress**: como aplicación principal.

### Requisitos previos

Asegúrate de tener instalado:

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)

### Instalación

1. **Clona este repositorio**:
   ```bash
   git clone https://github.com/tu-usuario/docker-compose-wordpress.git
   cd docker-compose-wordpress
2. **Ejecuta Docker Compose: En la carpeta del repositorio, ejecuta:
   ```bash
   docker-compose up -d
Este comando descargará las imágenes necesarias (si no están descargadas) y iniciará los contenedores en modo desacoplado.

## Servicios y puertos

* **WordPress**: http://localhost:8083
* **PhpMyAdmin**: http://localhost:8082
* **Usuario**: eddevios
* **Contraseña**: 123456

## Configuración del entorno

El archivo `docker-compose.yml` configura lo siguiente:

* **Base de datos de MariaDB**:
	+ Nombre de la base de datos: db_eddevios
	+ Usuario: eddevios
	+ Contraseña: 123456
	+ Contraseña de root: root123
* **Configuración de WordPress**:
	+ WordPress se conecta al contenedor de base de datos de MariaDB utilizando las credenciales anteriores.

## Volúmenes

Esta configuración incluye volúmenes para persistir datos:

* `db_data`: almacena los datos de la base de datos de MariaDB
* `wordpress_data`: almacena los archivos de WordPress

## Deteniendo los contenedores

Para detener los contenedores, ejecuta:
  ```bash
  docker-compose down
```
# Resolución de problemas
Errores de conexión a la base de datos: asegúrate de que las variables de entorno PMA_HOST, WORDPRESS_DB_HOST y otras en docker-compose.yml estén configuradas correctamente.
Conflictos de puertos: cambia los mapeos de puertos en docker-compose.yml si estos puertos ya están en uso.

# Licencia
## Este proyecto está licenciado bajo la Licencia GNU General Public License v3.0.
