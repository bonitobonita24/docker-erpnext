
[uri_license]: http://www.gnu.org/licenses/agpl.html
[uri_license_image]: https://img.shields.io/badge/License-AGPL%20v3-blue.svg

[![License: AGPL v3][uri_license_image]][uri_license]
[![Build Status](https://travis-ci.org/Monogramm/docker-erpnext.svg)](https://travis-ci.org/Monogramm/docker-erpnext)
[![Docker Automated buid](https://img.shields.io/docker/cloud/build/monogramm/docker-erpnext.svg)](https://hub.docker.com/r/monogramm/docker-erpnext/)
[![Docker Pulls](https://img.shields.io/docker/pulls/monogramm/docker-erpnext.svg)](https://hub.docker.com/r/monogramm/docker-erpnext/)
[![](https://images.microbadger.com/badges/version/monogramm/docker-erpnext.svg)](https://microbadger.com/images/monogramm/docker-erpnext)
[![](https://images.microbadger.com/badges/image/monogramm/docker-erpnext.svg)](https://microbadger.com/images/monogramm/docker-erpnext)

# ERPNext Docker container

Docker image for ERPNext.

This image was inspired by several other containers developed by the community:
* [emadshaaban92/docker-compose-erpnext](https://github.com/emadshaaban92/docker-compose-erpnext/) / [BizzoTech/docker-erpnext](https://github.com/BizzoTech/docker-erpnext) for the "_simple_" docker-compose setup
* [donysukardi/docker-frappe](https://github.com/donysukardi/docker-frappe) for the alpine variant (actually the source for BizzoTech images)
* [pipech/erpnext-docker-debian](https://github.com/pipech/erpnext-docker-debian) for the complete setup of apps and sites

The concept is the following:
* no need to provide any configuration file: everything will be automatically generated by the container through environnment variables
* the application container sets all the environment variables, the other containers wait for setup to be done
* provide postgresql compatibility

Check base image [Monogramm/docker-frappe](https://github.com/Monogramm/docker-frappe) for details.

Check image [Monogramm/docker-erpnext-ext](https://github.com/Monogramm/docker-erpnext-ext) to see how to expand this image and add custom frappe apps.

:warning: **This image is still in beta and should not be used in production (yet)!**

## What is ERPNext ?

Open Source ERP built for the web.

> [erpnext.com](https://erpnext.com/)

> [github erpnext](https://github.com/frappe/erpnext)

## Supported tags

https://hub.docker.com/r/monogramm/docker-erpnext/

* ERPNext develop branch
    - `develop-alpine` `develop`
    - `develop-debian` `develop-stretch`
    - `develop-debian-slim` `develop-stretch-slim`
* ERPNext 11
    - `11-alpine` `11` `alpine` `latest`
    - `11-debian` `debian` `11-stretch` `stretch`
    - `11-debian-slim` `debian-slim` `11-stretch-slim` `stretch-slim`
* ERPNext 10 (branch 10.x.x for latest bug fixes)
    - `10-alpine` `10`
    - `10-debian` `10-stretch`
    - `10-debian-slim` `10-stretch-slim`

# Questions / Issues
If you got any questions or problems using the image, please visit our [Github Repository](https://github.com/Monogramm/docker-erpnext) and write an issue.  

# References

A list of a few issues encountered during the development of this container for future reference:
* ERPNext installs fails with Postgresql due to missing column
    * _Solution_: none so far...
    * _References_:
        * https://github.com/frappe/erpnext/issues/18028

