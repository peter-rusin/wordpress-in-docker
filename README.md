# Wordpress In Docker

Minimalistic boilerplate repository for the WordPress themes / plugins development using Docker.

## Prerequisites

* [Docker](https://docs.docker.com/engine/install/)
* [Docker Compose](https://docs.docker.com/compose/install/)

## Initial setup

Rename `.env.example` to `.env` and adjust it accordingly.

Docker Compose is supporting `.env` files out of the box.

## Starting a web server

Run: `docker-compose up`

## Installing exising themes / plugins

WordPress Packagist: https://wpackagist.org/

For plugins:
```
 docker run --rm --interactive --tty \
  --volume $PWD:/app \
  --user $(id -u):$(id -g) \
  composer require wpackagist-plugin/plugin-slug
```

For themes:
```
 docker run --rm --interactive --tty \
  --volume $PWD:/app \
  --user $(id -u):$(id -g) \
  composer require wpackagist-theme/theme-slug
```
