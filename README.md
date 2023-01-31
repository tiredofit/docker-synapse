# github.com/tiredofit/synapse

[![GitHub release](https://img.shields.io/github/v/tag/tiredofit/synapse?style=flat-square)](https://github.com/tiredofit/synapse/releases/latest)
[![Build Status](https://img.shields.io/github/actions/workflow/status/tiredofit/docker-synapse/main.yml?branch=main&style=flat-square)](https://github.com/tiredofit/docker-synapse/actions)
[![Docker Stars](https://img.shields.io/docker/stars/tiredofit/synapse.svg?style=flat-square&logo=docker)](https://hub.docker.com/r/tiredofit/synapse/)
[![Docker Pulls](https://img.shields.io/docker/pulls/tiredofit/synapse.svg?style=flat-square&logo=docker)](https://hub.docker.com/r/tiredofit/synapse/)
[![Become a sponsor](https://img.shields.io/badge/sponsor-tiredofit-181717.svg?logo=github&style=flat-square)](https://github.com/sponsors/tiredofit)
[![Paypal Donate](https://img.shields.io/badge/donate-paypal-00457c.svg?logo=paypal&style=flat-square)](https://www.paypal.me/tiredofit)

## About

This will build a Docker Image for [Synapse] (https://matrix.org/docs/projects/server/synapse), A Matrix.org Homeserver

## Maintainer

- [Dave Conroy](https://github.com/tiredofit/)

## Table of Contents

- [About](#about)
- [Maintainer](#maintainer)
- [Table of Contents](#table-of-contents)
- [Installation](#installation)
  - [Build from Source](#build-from-source)
  - [Prebuilt Images](#prebuilt-images)
    - [Multi Architecture](#multi-architecture)
- [Configuration](#configuration)
  - [Quick Start](#quick-start)
  - [Persistent Storage](#persistent-storage)
  - [Environment Variables](#environment-variables)
    - [Base Images used](#base-images-used)
  - [Networking](#networking)
- [Maintenance](#maintenance)
  - [Shell Access](#shell-access)
- [Support](#support)
  - [Usage](#usage)
  - [Bugfixes](#bugfixes)
  - [Feature Requests](#feature-requests)
  - [Updates](#updates)
- [License](#license)
- [References](#references)

## Installation
### Build from Source
Clone this repository and build the image with `docker build -t (imagename) .`

### Prebuilt Images
Builds of the image are available on [Docker Hub](https://hub.docker.com/r/tiredofit/synapse)

```bash
docker pull docker.io/tiredofdit/synapse:(imagetag)
```
Builds of the image are also available on the [Github Container Registry](https://github.com/tiredofit/docker-synapse/pkgs/container/docker-synapse) 
 
```
docker pull ghcr.io/tiredofit/docker-synapse:(imagetag)
``` 

The following image tags are available along with their tagged release based on what's written in the [Changelog](CHANGELOG.md):

| Container OS | Tag       |
| ------------ | --------- |
| Alpine       | `:latest` |

#### Multi Architecture
Images are built primarily for `amd64` architecture, and may also include builds for `arm/v7`, `arm64` and others. These variants are all unsupported. Consider [sponsoring](https://github.com/sponsors/tiredofit) my work so that I can work with various hardware. To see if this image supports multiple architecures, type `docker manifest (image):(tag)`

## Configuration

### Quick Start

* The quickest way to get started is using [docker-compose](https://docs.docker.com/compose/). See the examples folder for a working [docker-compose.yml](examples/docker-compose.yml) that can be modified for development or production use.

* Set various [environment variables](#environment-variables) to understand the capabilities of this image.
* Map [persistent storage](#data-volumes) for access to configuration and data files for backup.

### Persistent Storage

The following directories are used for configuration and can be mapped for persistent storage.

| Directory | Description |
| --------- | ----------- |


* * *
### Environment Variables

#### Base Images used

This image relies on an [Alpine Linux](https://hub.docker.com/r/tiredofit/alpine) base image that relies on an [init system](https://github.com/just-containers/s6-overlay) for added capabilities. Outgoing SMTP capabilities are handlded via `msmtp`. Individual container performance monitoring is performed by [zabbix-agent](https://zabbix.org). Additional tools include: `bash`,`curl`,`less`,`logrotate`,`nano`,`vim`.

Be sure to view the following repositories to understand all the customizable options:

| Image                                                  | Description                            |
| ------------------------------------------------------ | -------------------------------------- |
| [OS Base](https://github.com/tiredofit/docker-alpine/) | Customized Image based on Alpine Linux |

| Variable | Description | Default |
| -------- | ----------- | ------- |

### Networking


| Port   | Protocol | Description        |
| ------ | -------- | ------------------ |
| `8008` | `tcp`    | Synapse Homeserver |
## Maintenance
### Shell Access

For debugging and maintenance purposes you may want access the containers shell.

```bash
docker exec -it (whatever your container name is) bash
```
## Support

These images were built to serve a specific need in a production environment and gradually have had more functionality added based on requests from the community.
### Usage
- The [Discussions board](../../discussions) is a great place for working with the community on tips and tricks of using this image.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) for personalized support
### Bugfixes
- Please, submit a [Bug Report](issues/new) if something isn't working as expected. I'll do my best to issue a fix in short order.

### Feature Requests
- Feel free to submit a feature request, however there is no guarantee that it will be added, or at what timeline.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) regarding development of features.

### Updates
- Best effort to track upstream changes, More priority if I am actively using the image in a production environment.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) for up to date releases.

## License
MIT. See [LICENSE](LICENSE) for more details.

## References

* <https://matrix.org/docs/projects/server/synapse>
# github.com/tiredofit/synapse

[![GitHub release](https://img.shields.io/github/v/tag/tiredofit/synapse?style=flat-square)](https://github.com/tiredofit/synapse/releases/latest)
[![Build Status](https://img.shields.io/github/actions/workflow/status/tiredofit/docker-synapse/main.yml?branch=main&style=flat-square)](https://github.com/tiredofit/docker-synapse/actions)
[![Docker Stars](https://img.shields.io/docker/stars/tiredofit/synapse.svg?style=flat-square&logo=docker)](https://hub.docker.com/r/tiredofit/synapse/)
[![Docker Pulls](https://img.shields.io/docker/pulls/tiredofit/synapse.svg?style=flat-square&logo=docker)](https://hub.docker.com/r/tiredofit/synapse/)
[![Become a sponsor](https://img.shields.io/badge/sponsor-tiredofit-181717.svg?logo=github&style=flat-square)](https://github.com/sponsors/tiredofit)
[![Paypal Donate](https://img.shields.io/badge/donate-paypal-00457c.svg?logo=paypal&style=flat-square)](https://www.paypal.me/tiredofit)

## About

This will build a Docker Image for [Synapse] (https://matrix.oprg/docs/projects/server/synapse), A Matrix.org Homeserver

## Maintainer

- [Dave Conroy](https://github.com/tiredofit/)

## Table of Contents

- [About](#about)
- [Maintainer](#maintainer)
- [Table of Contents](#table-of-contents)
- [Installation](#installation)
  - [Build from Source](#build-from-source)
  - [Prebuilt Images](#prebuilt-images)
    - [Multi Architecture](#multi-architecture)
- [Configuration](#configuration)
  - [Quick Start](#quick-start)
  - [Persistent Storage](#persistent-storage)
  - [Environment Variables](#environment-variables)
    - [Base Images used](#base-images-used)
  - [Networking](#networking)
- [Maintenance](#maintenance)
  - [Shell Access](#shell-access)
- [Support](#support)
  - [Usage](#usage)
  - [Bugfixes](#bugfixes)
  - [Feature Requests](#feature-requests)
  - [Updates](#updates)
- [License](#license)
- [References](#references)


## Installation
### Build from Source
Clone this repository and build the image with `docker build -t (imagename) .`

### Prebuilt Images
Builds of the image are available on [Docker Hub](https://hub.docker.com/r/tiredofit/synapse)

```bash
docker pull docker.io/tiredofdit/synapse:(imagetag)
```
Builds of the image are also available on the [Github Container Registry](https://github.com/tiredofit/docker-synapse/pkgs/container/docker-synapse) 
 
```
docker pull ghcr.io/tiredofit/docker-synapse:(imagetag)
``` 

The following image tags are available along with their tagged release based on what's written in the [Changelog](CHANGELOG.md):

| Container OS | Tag       |
| ------------ | --------- |
| Alpine       | `:latest` |

#### Multi Architecture
Images are built primarily for `amd64` architecture, and may also include builds for `arm/v7`, `arm64` and others. These variants are all unsupported. Consider [sponsoring](https://github.com/sponsors/tiredofit) my work so that I can work with various hardware. To see if this image supports multiple architecures, type `docker manifest (image):(tag)`

## Configuration

### Quick Start

* The quickest way to get started is using [docker-compose](https://docs.docker.com/compose/). See the examples folder for a working [compose.yml](examples/compose.yml) that can be modified for development or production use.

* Set various [environment variables](#environment-variables) to understand the capabilities of this image.
* Map [persistent storage](#data-volumes) for access to configuration and data files for backup.

### Persistent Storage

The following directories are used for configuration and can be mapped for persistent storage.

| Directory         | Description         |
| ----------------- | ------------------- |
| `/data/certs/`    | Signing Keys        |
| `/data/config`    | Configuration Files |
| `/data/media`     | Media / Assets      |
| `/data/templates` | Email Templates     |
| `/data/uploads`   | Uploaded Assets     |
| `/logs`           | Log files           |

* * *
### Environment Variables

#### Base Images used

This image relies on an [Alpine Linux](https://hub.docker.com/r/tiredofit/alpine) base image that relies on an [init system](https://github.com/just-containers/s6-overlay) for added capabilities. Outgoing SMTP capabilities are handlded via `msmtp`. Individual container performance monitoring is performed by [zabbix-agent](https://zabbix.org). Additional tools include: `bash`,`curl`,`less`,`logrotate`,`nano`,`vim`.

Be sure to view the following repositories to understand all the customizable options:

| Image                                                  | Description                            |
| ------------------------------------------------------ | -------------------------------------- |
| [OS Base](https://github.com/tiredofit/docker-alpine/) | Customized Image based on Alpine Linux |

#### Container Options

| Variable             | Description                                          | Default                  |
| -------------------- | ---------------------------------------------------- | ------------------------ |
| `CERT_PATH`          | Signing Key Path                                     | `${DATA_PATH}/certs/`    |
| `CONFIG_FILE`        | Configuration File                                   | `homeserver.yaml`        |
| `CONFIG_PATH`        | Configuration File path                              | `${DATA_PATH}/config/`   |
| `DATA_PATH`          | Data Path                                            | `/data/`                 |
| `LOG_FORMAT`         | What format of logs `STANDARD` or `JSON`             | `STANDARD`               |
| `LOG_FORMAT_CONSOLE` | What format of logs `STANDARD` or `JSON` for console | `${LOG_FORMAT}`          |
| `LOG_FORMAT_FILE`    | What format of logs `STANDARD` or `JSON` for file    | `${LOG_FORMAT}`          |
| `LOG_PATH`           | Log file path                                        | `/logs/`                 |
| `LOG_TYPE`           | How to display logs `FILE`,`CONSOLE` or `BOTH`       | `FILE`                   |
| `MEDIA_PATH`         | Media / Assets path                                  | `${DATA_PATH}/media`     |
| `SETUP_MODE`         | Update configuration based on environment variables  | `AUTO`                   |
| `TEMPLATE_PATH`      | Email Templates                                      | `${DATA_PATH}/templates` |
| `UPLOAD_PATH`        | Uploads Path                                         | `${DATA_PATH}/uploads`   |

#### Application Options

| Variable                                | Description                           | Default                  |
| --------------------------------------- | ------------------------------------- | ------------------------ |
| `CREATE_ADMIN_USER`                     | Create Admin User on Startup          | `TRUE`                   |
| `ADMIN_PASS`                            | Admin Password                        | `tiredofit`              |
| `ADMIN_USER`                            | Admin User Name                       | `synapse`                |
| `CONTACT_ADMIN_EMAIL`                   | Admin Contact Email                   | `admin@example.com`      |
| `ENABLE_HTTP`                           | Enable HTTP Listeners                 | `TRUE`                   |
| `ENABLE_METRICS`                        | Enable Metrics Listeners              | `TRUE`                   |
| `HTTP_ENABLE_COMPRESSION`               | Enable Compression                    | `TRUE`                   |
| `HTTP_ENABLE_TLS`                       | Enable TLS Services                   | `FALSE`                  |
| `HTTP_ENABLE_X_FORWARDED`               |                                       | `TRUE`                   |
| `HTTP_LISTEN_IP`                        | HTTP Listen Port                      | `0.0.0.0`                |
| `HTTP_LISTEN_PORT`                      | HTTP Listen Port                      | `8008`                   |
| `HTTP_MODE`                             | What resources to offer               | `client,federation`      |
| `LOG_BUFFER`                            |                                       | `10`                     |
| `LOG_FILE`                              | Log File                              | `homeserver.log`         |
| `LOG_INTERVAL_FLUSH_FORCE`              |                                       | `5`                      |
| `LOG_LEVEL_FLUSH`                       |                                       | `30`                     |
| `LOG_LEVEL_LDAP_AUTH_PROVIDER`          | Log LDAP Auth Provider Level          | `${LOG_LEVEL}`           |
| `LOG_LEVEL_LDAP`                        | Log LDAP Level                        | `${LOG_LEVEL}`           |
| `LOG_LEVEL_SHARED_SECRET_AUTHENTICATOR` | Log Shared Secret Authenticator Level | `${LOG_LEVEL}`           |
| `LOG_LEVEL_SQL`                         | Log SQL Level                         | `${LOG_LEVEL}`           |
| `LOG_LEVEL`                             | Log Level                             | `INFO`                   |
| `METRICS_LISTEN_IP`                     | Metrics Listen IP                     | `127.0.0.1`              |
| `METRICS_LISTEN_PORT`                   | HTTP Listen Port                      | `8009`                   |
| `SECRET_FORM`                           | Form secret                           | (autogenerated)          |
| `SECRET_MACAROON`                       | Macaroon secret                       | (autogenerated)          |
| `SECRET_REGISTRATION`                   | Registration secret                   | (autogenerated)          |
| `SERVER_NAME`                           | Server name eg `example.com`          |                          |
| `SERVER_URL`                            | Server URL eg `https://example.com`   | `https://${SERVER_NAME}` |

#### Database Options

| Variable                    | Description                           | Default                |
| --------------------------- | ------------------------------------- | ---------------------- |
| `DB_SQLITE_NAME`            | (sqlite) Database name                | `homeserver.db`        |
| `DB_SQLITE_PATH`            | (sqlite) Database Path                | `${DATA_PATH}/sqlite/` |
| `DB_POOL_MAX`               | (postgres)                            | `10`                   |
| `DB_POOL_MIN`               | (postgres)                            | `5`                    |
| `DB_TRANSACTION_LIMIT`      | (postgres)                            | `10000`                |
| `DB_HOST`                   | (postgres) Postgresql Hostname        |                        |
| `DB_KEEP_ALIVE_INTERVAL_MS` | (postgres) Keep alive in milliseconds | `30000`                |
| `DB_NAME`                   | (postgres)  Postgresql Name           |                        |
| `DB_PASS`                   | (postgres)  Postgresql Password       |                        |
| `DB_PORT`                   | (postgres)  Postgresql Port           | `5432`                 |
| `DB_TYPE`                   | Database type `postgres` or `sqlite`  | `POSTGRES`             |
| `DB_USER`                   | (postgres)  Postgresql User           |                        |

### Networking

| Port   | Protocol | Description        |
| ------ | -------- | ------------------ |
| `8008` | `tcp`    | Synapse Homeserver |

## Maintenance
### Shell Access

For debugging and maintenance purposes you may want access the containers shell.

```bash
docker exec -it (whatever your container name is) bash
```
## Support

These images were built to serve a specific need in a production environment and gradually have had more functionality added based on requests from the community.
### Usage
- The [Discussions board](../../discussions) is a great place for working with the community on tips and tricks of using this image.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) for personalized support
### Bugfixes
- Please, submit a [Bug Report](issues/new) if something isn't working as expected. I'll do my best to issue a fix in short order.

### Feature Requests
- Feel free to submit a feature request, however there is no guarantee that it will be added, or at what timeline.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) regarding development of features.

### Updates
- Best effort to track upstream changes, More priority if I am actively using the image in a production environment.
- Consider [sponsoring me](https://github.com/sponsors/tiredofit) for up to date releases.

## License
MIT. See [LICENSE](LICENSE) for more details.

## References

* <https://matrix.org/docs/projects/server/synapse>
