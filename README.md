PHP for Drupal
=============

- Apache
- PHP
- extensionsions required by Drupal (mbstring, opcache, pdo_mysql, gd)

# Quickstart:

PHP7 + Apache
````
docker run -dP --volume /path/to/drupal:/var/www/html zaporylie/php-drupal:7-apache
````

PHP5.6 + Apache
````
docker run -dP --volume /path/to/drupal:/var/www/html zaporylie/php-drupal:5.6-apache
````

# Versions (Docker tags):
- `5.4-apache`, `5.4`
- `5.5-apache`, `5.5`
- `5.6-apache`, `5.6`, `latest`
- `7-apache`, `7`

# Status
Proof of concept
