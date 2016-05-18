PHP for Drupal
=====================
[![Build Status](https://travis-ci.org/drupal-docker/php.svg?branch=master)](https://travis-ci.org/drupal-docker/php)

Version | Type | Tags | Dockerfile
--- | --- | --- | ---
5.4 | cli | `5.4-cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.4/Dockerfile)
5.4 | apache | `5.4-apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.4/apache/Dockerfile)
5.4 | fpm | `5.4-fpm`, `5.4` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.4/fpm/Dockerfile)
5.5 | cli | `5.5-cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.5/Dockerfile)
5.5 | apache | `5.5-apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.5/apache/Dockerfile)
5.5 | fpm | `5.5-fpm`, `5.5` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.5/fpm/Dockerfile)
5.6 | cli | `5.6-cli`, `5-cli`, `cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.6/Dockerfile)
5.6 | apache | `5.6-apache`, `5-apache`, `apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.6/apache/Dockerfile)
5.6 | fpm | `5.6-fpm`, `5-fpm`, `5.6`, `5`, `fpm`, `latest` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/5.6/fpm/Dockerfile)
7.0 | cli | `7.0-cli`, `7-cli` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/7.0/Dockerfile)
7.0 | apache | `7.0-apache`, `7-apache` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/7.0/apache/Dockerfile)
7.0 | fpm | `7.0-fpm`, `7.fpm`, `7.0`, `7` | [Dockerfile](https://github.com/drupal-docker/php/blob/master/7.0/fpm/Dockerfile)

# Quickstart:

PHP 5.6 + Apache
```bash
docker run -dP drupaldocker/php:apache
```

# Environmental variables

No variables

# Description

@todo

# Status

Proof of concept

# Contributing

1. Fork the repo
1. Create your feature branch
1. Commit your changes
1. Push to the branch
1. Create new Pull Request
1. Wait for result of automate tests

# Credits
`drupaldocker/php images were built on the top of official [PHP images](https://hub.docker.com/r/_/php/). Big kudos to people from Docker community for official [Drupal image](https://hub.docker.com/r/_/drupal/).
