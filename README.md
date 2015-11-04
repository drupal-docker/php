PHP for Drupal
=============

- Apache + mod_php
- PHP-FPM

# Quickstart:

PHP5.6 + Apache (mod_php)
````
docker run -dP --volume /path/to/drupal:/var/www/html drupal-docker/php:apache
````

# Versions (Docker tags):
- `5.4-apache` ([Dockerfile](https://github.com/drupal-docker/php/blob/master/apache/5.4/Dockerfile))
- `5.5-apache` ([Dockerfile](https://github.com/drupal-docker/php/blob/master/apache/5.5/Dockerfile))
- `5.6-apache`, `5-apache`, `apache`, `latest` ([Dockerfile](https://github.com/drupal-docker/php/blob/master/apache/5.6/Dockerfile))
- `7-apache` ([Dockerfile](https://github.com/drupal-docker/php/blob/master/apache/7/Dockerfile))
- `5.4-fpm`, `5.4` ([Dockerfile](https://github.com/drupal-docker/php/blob/master/fpm/5.4/Dockerfile))
- `5.5-fpm`, `5.5` ([Dockerfile](https://github.com/drupal-docker/php/blob/master/fpm/5.5/Dockerfile))
- `5.6-fpm`, `5-fpm`, `5.6`, `5`, `fpm`, `latest`  ([Dockerfile](https://github.com/drupal-docker/php/blob/master/fpm/5.6/Dockerfile))
- `7-fpm`, `7` ([Dockerfile](https://github.com/drupal-docker/php/blob/master/fpm/7/Dockerfile))

# Roadmap
- ~~Add Dockerfiles for PHP + Apache (mod_php)~~
- ~~Add Dockerfiles for PHP-FPM~~
- ~~Make Apache powered images default ones~~
- ~~Default version (latest): Apache + PHP5.6~~
- ~~Make FPM _tags_ default (`5.6-fpm`, `5.6`, `latest`)~~
- Add php-cli (with Drush?)
- Create drupal-docker/nginx
- Create drupal-docker/apache

# Status
Proof of concept

# Credits
Drupal PHP images where built on the top of official [PHP images](https://hub.docker.com/r/_/php/). Thanks to people from Docker community for official [Drupal image](https://hub.docker.com/r/_/drupal/).
