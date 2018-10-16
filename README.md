# Small Docker Image

[![Docker Pulls](https://img.shields.io/docker/pulls/arcaneio/mini.svg?style=flat)](https://hub.docker.com/r/arcaneio/mini/)
[![Docker Automated build](https://img.shields.io/docker/automated/arcaneio/mini.svg?style=flat)](https://hub.docker.com/r/arcaneio/mini/)
[![Docker Build Status](https://img.shields.io/docker/build/arcaneio/mini.svg?style=flat)](https://hub.docker.com/r/arcaneio/mini/)
[![license](https://img.shields.io/github/license/arcane-io/docker-mini.svg)](https://github.com/arcane-io/docker-mini)

Docker min is a small docker image (<https://hub.docker.com/r/arcaneio/mini/>) based on `alpine` which allows for easy configuration of multiple services using [supervisord](http://supervisord.org/configuration.html).

## Adding services

1. add service configuration to /etc/supervisord.d
2. service configuration file name should have the extension 'conf'

## Configuration example

```conf
[program:my-app]
user=root
command=command-to-run.sh
redirect_stderr=true
stdout_logfile=/var/log/my-app.log
autorestart=true
startretries=3
```
