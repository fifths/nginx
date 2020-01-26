# Nginx Brotli Docker Image

[![Build Status](https://travis-ci.org/fifths/nginx.svg?branch=master)](https://travis-ci.org/fifths/nginx)
[![Docker Automated build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/fifths/nginx)

## Supported branches 
- 1.16: `1.16.1`
- 1.17: `1.17.8`、`1.17.7`、`1.17.6`、`1.17.5`、`1.17.4`、`1.17.3`、


## Getting image

```sh
docker pull fifths/nginx
```

## nginx.conf

```conf 
load_module  modules/ngx_http_brotli_filter_module.so;
load_module  modules/ngx_http_brotli_static_module.so;

user  nginx;
worker_processes  auto;

error_log  /var/log/nginx/error.log warn;
pid        /var/run/nginx.pid;

events {
  ...
}

http {
  ...
}
```
