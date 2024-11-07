# DDEV imgproxy

## What is this?

This repository allows you to quickly install an [imgproxy](https://imgproxy.net/) server into a [DDEV](https://ddev.readthedocs.io) project using the instructions below.

imgproxy is a standalone server for resizing, processing and converting images. With imgproxy you can quickly and easily edit images on the fly (resize, crop, watermark, filter,...), convert them to other file formats, optimise images and more.

In addition to the paid version, the free, self-hosted version of imgproxy (open source) can also be used without registration or further steps. Of course, there are differences between the open source and the pro version, which are described on the [imgproxy features](https://imgproxy.net/features/) page. 

## Installation

Uses [imgproxy official image](https://hub.docker.com/r/darthsim/imgproxy/)


```sh
ddev add-on get barbieswimcrew/ddev-imgproxy && ddev restart
```

For earlier versions of DDEV run

```sh
ddev get barbieswimcrew/ddev-imgproxy && ddev restart
```


Navigating https://localhost:8081 should display the imgproxy default landingpage.

## Explanation

This recipe for [DDEV](https://ddev.readthedocs.io) installs a [.ddev/docker-compose.imgproxy.yaml](docker-compose.imgproxy.yaml) using the `darthsim/imgproxy` Docker image.

As soon as imgproxy is running successfully, requests can be sent to imgproxy to convert images from a source format to the desired target format. A prominent scenario for this is the generation of thumbnails:

```
https://localhost:8081/insecure/size:360:240/plain//web/path/to/image.png@avif
```

This request would convert/return the file `web/path/to/image.png` into an AVIF thumbnail with the desired dimensions 360x240px.

**Contributed and maintained by [@barbieswimcrew](https://github.com/barbieswimcrew)**
