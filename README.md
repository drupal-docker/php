PHP for Drupal
=============

- Apache
- PHP
- extensionsions required by Drupal (mbstring, opcache, pdo_mysql, pdo_pgsql, gd)

# Quickstart:

PHP7 + Apache (mod_php)
````
docker run -dP --volume /path/to/drupal:/var/www/html zaporylie/php-drupal:7-apache
````

PHP5.6 + Apache (mod_php)
````
docker run -dP --volume /path/to/drupal:/var/www/html zaporylie/php-drupal:5.6-apache
````

# Versions (Docker tags):
- `5.4-apache`, `5.4` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/apache/5.4/Dockerfile))
- `5.5-apache`, `5.5` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/apache/5.5/Dockerfile))
- `5.6-apache`, `5.6`, `latest` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/apache/5.6/Dockerfile))
- `7-apache`, `7` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/apache/7/Dockerfile))
- `5.4-fpm` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/fpm/5.4/Dockerfile))
- `5.5-fpm` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/fpm/5.5/Dockerfile))
- `5.6-fpm` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/fpm/5.6/Dockerfile))
- `7-fpm` ([Dockerfile](https://github.com/zaporylie/docker-php-drupal/blob/master/fpm/7/Dockerfile))

# Roadmap
- ~~Add Dockerfiles for PHP + Apache (mod_php)~~
- ~~Add Dockerfiles for PHP-FPM~~
- ~~Make Apache powered images default ones~~
- ~~Default version (latest): Apache + PHP5.6~~
- Create zaporylie/docker-nginx-drupal
- Create zaporylie/docker-apache-drupal
- Make FPM _tags_ default (`5.6-fpm`, `5.6`, `latest`)

# Status
Proof of concept

# Credits
Drupal PHP images where built on the top of official [PHP images](https://hub.docker.com/r/_/php/). Thanks to people from Docker community for official [Drupal image](https://hub.docker.com/r/_/drupal/).
