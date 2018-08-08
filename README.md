# About this Repo

[![Build Status](https://travis-ci.org/anaxexp/base-php.svg?branch=master)](https://travis-ci.org/anaxexp/base-php)
[![Docker Pulls](https://img.shields.io/docker/pulls/anaxexp/base-php.svg)](https://hub.docker.com/r/anaxexp/base-php)
[![Docker Stars](https://img.shields.io/docker/stars/anaxexp/base-php.svg)](https://hub.docker.com/r/anaxexp/base-php)
[![Docker Layers](https://images.microbadger.com/badges/image/anaxexp/base-php.svg)](https://microbadger.com/images/anaxexp/base-php)

This repository is a fork of https://github.com/docker-library/php with a few changes:

* We build only Alpine FPM variants
* Built with LibreSSL instead of OpenSSL
* Additional debug variants of images with --enable-debug and non-stripped bins
* Legacy PHP 5.3 variant

## Docker Images

* All images are based on Alpine Linux 3.7 (except legacy 5.3 on Alpine 3.4)
* Base image: [anaxexp/alpine](https://github.com/anaxexp/alpine)
* [Travis CI builds](https://travis-ci.org/anaxexp/base-php) 
* [Docker Hub](https://hub.docker.com/r/anaxexp/base-php)

[_(Dockerfile 7.2)_]: https://github.com/anaxexp/base-php/tree/master/7.2/alpine3.7/fpm/Dockerfile.anaxexp
[_(Dockerfile 7.1)_]: https://github.com/anaxexp/base-php/tree/master/7.1/alpine3.7/fpm/Dockerfile.anaxexp
[_(Dockerfile 7.0)_]: https://github.com/anaxexp/base-php/tree/master/7.0/alpine3.7/fpm/Dockerfile.anaxexp
[_(Dockerfile 5.6)_]: https://github.com/anaxexp/base-php/tree/master/5.6/alpine3.7/fpm/Dockerfile.anaxexp
[_(Dockerfile 5.3)_]: https://github.com/anaxexp/base-php/tree/master/5.3/alpine3.4/fpm/Dockerfile.anaxexp

Supported tags and respective `Dockerfile` links:

* `7.2.8`, `7.2`, `7`, `latest` [_(Dockerfile 7.2)_]
* `7.1.20`, `7.1` [_(Dockerfile 7.1)_]
* `7.0.31`, `7.0` [_(Dockerfile 7.0)_]
* `5.6.37`, `5.6`, `5` [_(Dockerfile 5.6)_]
* `5.3.29`, `5.3` [_(Dockerfile 5.3)_]
* `7.2.8-debug`, `7.2-debug`, `7-debug` [_(Dockerfile 7.2)_]
* `7.1.20-debug`, `7.1-debug` [_(Dockerfile 7.1)_]
* `7.0.31-debug`, `7.0-debug` [_(Dockerfile 7.0)_]
* `5.6.37-debug`, `5.6-debug`, `5-debug` [_(Dockerfile 5.6)_]

## Image with more PHP extensions and orchestration actions

See https://github.com/anaxexp/php
