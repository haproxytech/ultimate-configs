# HAProxy 2.2 Ultimate Configuration

### Overview

This is the HAProxy 2.2 ultimate configuration and it features a self-contained website that is 100% powered by HAProxy.

It does not rely on any 3rd party web applications, code, frameworks,or javascript.

#### How?

HAProxy 2.2 features a powerful native response generator that allows you to serve templates, which can contain complex formatted strings that are evaluated as it serves the request.

#### What does this mean?

You can now not only serve small image and static content directly from HAProxy to improve performance on small requested files, but you can also completely offload some of those requests directly to HAProxy.

### Examples

Builtin services:

* What is my IP?
* Digest
* Elephant facts

### Getting started - Docker
1. `export ULTCONFIG=$PWD` # specify the location of this repo
1. `docker run -p 7777:443 -p 7778:80  -v $ULTCONFIG:/usr/local/etc/haproxy:ro haproxytech/haproxy-ubuntu:2.2 -C /usr/local/etc/haproxy -f /usr/local/etc/haproxy/haproxy.cfg`
2. Navigate to
  - https http://dockerip:7777/
  - plain http: http://dockerip:7778/

### Getting started
* Install HAProxy 2.2
* clone this repo
* cd into repo directory
* haproxy -f haproxy.cfg -d
* Navigate to http://IP/ or https://IP/
