# Docker image with PHP 8 and Apache
## Download
You can download the lastest version using the following command
```bash
docker pull vcgtz/php
```
## Create Container
With the following command, you can create and start the container
```bash
docker run -it --name php -p 8080:80 -p 8000:8000 -v D:\Docker\Storage\php\:/code/ vcgtz/php
```
If you want to run again the container
```bash
docker start -i php
```