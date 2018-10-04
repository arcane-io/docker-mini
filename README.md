# Small Docker Image

[![Docker Pulls](https://img.shields.io/docker/pulls/arcaneio/docker-min.svg?style=flat)](https://hub.docker.com/r/arcaneio/docker-cron/)
[![Docker Automated build](https://img.shields.io/docker/automated/arcaneio/docker-min.svg?style=flat)](https://hub.docker.com/r/arcaneio/docker-min/)
[![Docker Build Status](https://img.shields.io/docker/build/arcaneio/docker-min.svg?style=flat)](https://hub.docker.com/r/arcaneio/docker-min/)
[![license](https://img.shields.io/github/license/arcane-io/docker-min.svg)](https://github.com/arcane-io/docker-min)

Docker min is a small docker image based on `alpine` which allows for easy configuration of multiple services.

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