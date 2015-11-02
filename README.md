PHP for Drupal
=============

- Apache
- PHP (5.6, 7)
- extensionsions required by Drupal (mbstring, opcache, pdo_mysql, gd)

# Quickstart:

PHP7 + Apache
````
docker run -dP --volume /path/to/drupal:/var/www/html zaporylie/php-drupal:7
````

PHP5.6 + Apache
````
docker run -dP --volume /path/to/drupal:/var/www/html zaporylie/php-drupal:5.6
````

# Status
Proof of concept
