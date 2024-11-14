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

## Para detener los contenedores, ejecuta:   
   ```bash
   docker-compose down

## Resolución de problemas

* **Errores de conexión a la base de datos**: asegúrate de que las variables de entorno `PMA_HOST`, `WORDPRESS_DB_HOST` y otras en `docker-compose.yml` estén configuradas correctamente.
* **Conflictos de puertos**: cambia los mapeos de puertos en `docker-compose.yml` si estos puertos ya están en uso.

## Licencia

Este proyecto está licenciado bajo la Licencia GNU General Public License v3.0.

Espero que esto te sea útil. Recuerda reemplazar "tu-usuario" con tu nombre de usuario de GitHub en la URL del repositorio.
