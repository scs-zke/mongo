# Container image build for mongo

This is a clone of the [Docker "Official Mongo Image"](https://github.com/docker-library/mongo). It is reduced to build just the 5.0.x image version for Linux.

This repository has been forked and the 5.0.x build reactivated to get a container image for 5.0.x with [CVE-2025-14847](https://www.cve.org/CVERecord?id=CVE-2025-14847) fixed. Mongo released a patch for the 5.0.x series as 5.0.32. Docker images for the 5.0.x series are not published anymore however since it is offically end-of-live.

## Usage

* Generate a new [versions.json](versions.json) by running ```versions.sh```. This will check the [Mongo Downloads](https://downloads.mongodb.org/current.json) for available version and generate a list of available versions.

* Generate the docker files by running ```apply-templates.sh```.

* Build the container images by running ```docker build .``` in the versions directories (i.e. in ```5.0```).
