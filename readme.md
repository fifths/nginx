# Nginx Brotli Docker Image

[![Build Status](https://travis-ci.org/fifths/nginx.svg?branch=master)](https://travis-ci.org/fifths/nginx)
[![Docker Automated build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/fifths/nginx)

## Supported branches 

- 1.17.3 [Dockerfile](https://github.com/fifths/nginx/blob/master/1.17.3/alpine3.10/Dockerfile)
- 1.17.4 [Dockerfile](https://github.com/fifths/nginx/blob/master/1.17.4/alpine3.10/Dockerfile)

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
