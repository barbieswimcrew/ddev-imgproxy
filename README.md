# DDEV imgproxy

## What is this?

This repository allows you to quickly install an [imgproxy](https://imgproxy.net/) server into a [DDEV](https://ddev.readthedocs.io) project using the instructions below.

## Installation

Uses [imgproxy official image](https://hub.docker.com/r/darthsim/imgproxy/)


```sh
ddev add-on get barbieswimcrew/ddev-imgproxy && ddev restart
```

For earlier versions of DDEV run

```sh
ddev get barbieswimcrew/ddev-imgproxy && ddev restart
```


Navigating http://localhost:8081 should display the imgproxy default landingpage.

## Explanation

This recipe for [DDEV](https://ddev.readthedocs.io) installs a [.ddev/docker-compose.imgproxy.yaml](docker-compose.imgproxy.yaml) using the `darthsim/imgproxy` Docker image.

**Contributed and maintained by [@barbieswimcrew](https://github.com/barbieswimcrew)**