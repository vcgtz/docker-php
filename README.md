# PHP Image for Development
Image with PHP 8.0, Apache and MariaDB (for development purposes only).

## Description
This image runs over Ubuntu 20.04 and contains the following tools:
* PHP 8.0
* Apache
* MariaDB
* Git
* Composer

## Download
To download this image you can use the following command:
```bash
docker pull vcgtz/php
```
## Create Container
With the image downloaded, you can create a container to start to work using the next command:
```
docker run -it --name <container_name> -p <port_1>:80 -p <port_2>:8000 -p <port_3>:3306 -v <host_work_directory>:/code/ vcgtz/php
```

* `<container_name>` is the name of your container
* `<port_1>` is the mapping of the port `80` in the container for Apache
* `<port_2>` is the mapping of the port `8000` in the container for Laravel Server
* `<port_3>` is the mapping of the port `3306` in the container for MariaDB
* `<host_working_dir>` is the working directory in the host machine

A real example:
```bash
docker run -it --name php_dev -p 8080:80 -p 8000:8000 -p 3306:3306 -v C:\Code\Projects\php_dev\:/code/ vcgtz/php
```
By default the working dir in the container is the folder `/code/` but you inside the container, you can move to `/var/www/html/` if you will use Apache.

## Start container
To start to working with the container, yo can use the following command:
```
docker start -i <container_name>
```
