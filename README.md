Minify Oracle instant client in Docker
======

This repository contains minify oracle-client based on debian image.
That consist of two version oracle instant client on basic and light version.


# NOTICE:

Support only x64 arch, linux os containers and oracle instant client version 12.1

[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)

## What is Oracle Instant client?

Free Oracle Database tools, libraries for building and connecting client applications to local or remote Oracle Database.

## Tags

* `12.1`
    * `basic` [12.1/basic](https://github.com/mrfoe7/minify-oracle-client/tree/master/12.1/basic)
        * `debian/jessie` [jessie/Dockerfile](https://github.com/mrfoe7/minify-oracle-client/blob/master/12.1/basic/jessie/Dockerfile)
        * `debian/stretch` [stretch/Dockerfile](https://github.com/mrfoe7/minify-oracle-client/blob/master/12.1/basic/stretch/Dockerfile)
    * `light` [12.1/light](https://github.com/mrfoe7/minify-oracle-client/tree/master/12.1/light)
        * `debian/jessie` [jessie/Dockerfile](https://github.com/mrfoe7/minify-oracle-client/blob/master/12.1/light/jessie/Dockerfile)
        * `debian/stretch` [stretch/Dockerfile](https://github.com/mrfoe7/minify-oracle-client/blob/master/12.1/light/stretch/Dockerfile)

* Official oracle instant client - [download](https://www.oracle.com/technetwork/topics/linuxx86-64soft-092277.html)

## How to install 

* Install [Docker](https://www.docker.com/get-started)
* Download image from [DockerHub](https://hub.docker.com/r/mrfoe7/minify-oracle-client)
* Usage this image and relax :lollipop: