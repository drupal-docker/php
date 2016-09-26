PHP-dev for Drupal
=====================
[![Build Status](https://travis-ci.org/drupal-docker/php.svg?branch=dev)](https://travis-ci.org/drupal-docker/php)
[![Docker Pulls](https://img.shields.io/docker/pulls/drupaldocker/php-dev.svg?maxAge=2592000)](https://hub.docker.com/r/drupaldocker/php-dev)

Version | Type | Tags | Dockerfile
--- | --- | --- | ---
5.4 (deprecated) | cli | `5.4-cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.4/Dockerfile)
5.4 (deprecated) | apache | `5.4-apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.4/apache/Dockerfile)
5.4 (deprecated) | fpm | `5.4-fpm`, `5.4` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.4/fpm/Dockerfile)
5.5 (deprecated) | cli | `5.5-cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.5/Dockerfile)
5.5 (deprecated) | apache | `5.5-apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.5/apache/Dockerfile)
5.5 (deprecated) | fpm | `5.5-fpm`, `5.5` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.5/fpm/Dockerfile)
5.6 | cli | `5.6-cli`, `5-cli`, `cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.6/Dockerfile)
5.6 | apache | `5.6-apache`, `5-apache`, `apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.6/apache/Dockerfile)
5.6 | fpm | `5.6-fpm`, `5-fpm`, `5.6`, `5`, `fpm`, `latest` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.6/fpm/Dockerfile)
7.0 | cli | `7.0-cli`, `7-cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/7.0/Dockerfile)
7.0 | apache | `7.0-apache`, `7-apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/7.0/apache/Dockerfile)
7.0 | fpm | `7.0-fpm`, `7.fpm`, `7.0`, `7` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/7.0/fpm/Dockerfile)
5.6-alpine | cli | `5.6-alpine-cli`, | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.6-alpine/Dockerfile)
5.6-apline | fpm | `5.6-alpine-fpm`,`5.6-alpine` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/5.6-alpine/fpm/Dockerfile)
7.0-alpine | cli | `7.0-alpine-cli`  | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/7.0-alpine/Dockerfile)
7.0-alpine | fpm | `7.0-alpinefpm`, `7.0-alpine` | [Dockerfile](https://github.com/drupal-docker/php/blob/dev/7.0-alpine/fpm/Dockerfile)

**Deprecation notice:** drupaldocker/php:5.4 and drupaldocker/php:5.5 EOL date: **December 13, 2016**

# Quickstart:

PHP 5.6 + Apache
```bash
docker run -dP drupaldocker/php-dev:apache
```

# Features

- xdebug

# More

Read more about PHP image in [master README](https://github.com/drupal-docker/php/blob/master/README.md).
