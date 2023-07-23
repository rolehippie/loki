# loki

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/loki)
[![General Workflow](https://github.com/rolehippie/loki/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/loki/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/loki/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/loki/actions/workflows/readme.yml)
[![Galaxy Workflow](https://github.com/rolehippie/loki/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/loki/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/loki)](https://github.com/rolehippie/loki/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.loki-blue)](https://galaxy.ansible.com/rolehippie/loki)

Ansible role to install and configure loki.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [loki_default_folders](#loki_default_folders)
  - [loki_default_labels](#loki_default_labels)
  - [loki_default_publish](#loki_default_publish)
  - [loki_default_volumes](#loki_default_volumes)
  - [loki_domain](#loki_domain)
  - [loki_extra_folders](#loki_extra_folders)
  - [loki_extra_labels](#loki_extra_labels)
  - [loki_extra_publish](#loki_extra_publish)
  - [loki_extra_volumes](#loki_extra_volumes)
  - [loki_image](#loki_image)
  - [loki_max_global_streams_per_user](#loki_max_global_streams_per_user)
  - [loki_max_streams_per_user](#loki_max_streams_per_user)
  - [loki_network](#loki_network)
  - [loki_oauth2_access_logging](#loki_oauth2_access_logging)
  - [loki_oauth2_allowed_groups](#loki_oauth2_allowed_groups)
  - [loki_oauth2_client_id](#loki_oauth2_client_id)
  - [loki_oauth2_client_secret](#loki_oauth2_client_secret)
  - [loki_oauth2_cookie_secret](#loki_oauth2_cookie_secret)
  - [loki_oauth2_default_labels](#loki_oauth2_default_labels)
  - [loki_oauth2_default_publish](#loki_oauth2_default_publish)
  - [loki_oauth2_extra_labels](#loki_oauth2_extra_labels)
  - [loki_oauth2_extra_publish](#loki_oauth2_extra_publish)
  - [loki_oauth2_image](#loki_oauth2_image)
  - [loki_oauth2_keycloak_url](#loki_oauth2_keycloak_url)
  - [loki_oauth2_listen_address](#loki_oauth2_listen_address)
  - [loki_oauth2_network](#loki_oauth2_network)
  - [loki_oauth2_provider](#loki_oauth2_provider)
  - [loki_oauth2_pull_image](#loki_oauth2_pull_image)
  - [loki_oauth2_request_logging](#loki_oauth2_request_logging)
  - [loki_oauth2_static_groups](#loki_oauth2_static_groups)
  - [loki_oauth2_static_users](#loki_oauth2_static_users)
  - [loki_oauth2_upstream](#loki_oauth2_upstream)
  - [loki_oauth2_version](#loki_oauth2_version)
  - [loki_pull_image](#loki_pull_image)
  - [loki_retention_time](#loki_retention_time)
  - [loki_version](#loki_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### loki_default_folders

List of default folders to create

#### Default value

```YAML
loki_default_folders:
  - /etc/loki
  - /var/lib/loki
```

### loki_default_labels

List of default labels to assign to docker

#### Default value

```YAML
loki_default_labels: []
```

### loki_default_publish

List of default port publishing for docker

#### Default value

```YAML
loki_default_publish: []
```

#### Example usage

```YAML
loki_default_publish:
  - 127.0.0.1:3100:3100
```

### loki_default_volumes

List of default volumes to mount for docker

#### Default value

```YAML
loki_default_volumes:
  - /var/lib/loki:/loki
  - /etc/loki:/etc/loki
```

### loki_domain

Domain for external access

#### Default value

```YAML
loki_domain:
```

#### Example usage

```YAML
loki_domain: https://loki.example.com
```

### loki_extra_folders

List of extra folders to create

#### Default value

```YAML
loki_extra_folders: []
```

#### Example usage

```YAML
loki_extra_folders:
  - /path/to/host/folder1
  - /path/to/host/folder2
  - /path/to/host/folder3
```

### loki_extra_labels

List of extra labels to assign to docker

#### Default value

```YAML
loki_extra_labels: []
```

### loki_extra_publish

List of extra port publishing for docker

#### Default value

```YAML
loki_extra_publish: []
```

#### Example usage

```YAML
loki_extra_publish:
  - 127.0.0.1:3100:3100
```

### loki_extra_volumes

List of extra volumes to mount for docker

#### Default value

```YAML
loki_extra_volumes: []
```

#### Example usage

```YAML
loki_extra_volumes:
  - /path/to/host/folder1:/path/within/container1
  - /path/to/host/folder2:/path/within/container2
  - /path/to/host/folder3:/path/within/container3
```

### loki_image

Docker image to use for deployment on OAuth2 Proxy

#### Default value

```YAML
loki_image: grafana/loki:{{ loki_version }}
```

### loki_max_global_streams_per_user

Limits config for max global streams per user

#### Default value

```YAML
loki_max_global_streams_per_user: 5000
```

### loki_max_streams_per_user

Limits config for max streams per user

#### Default value

```YAML
loki_max_streams_per_user: 0
```

### loki_network

Optional docker network to attach on OAuth2 Proxy

#### Default value

```YAML
loki_network:
```

### loki_oauth2_access_logging

Enable access logging for OAuth2 proxy

#### Default value

```YAML
loki_oauth2_access_logging: false
```

### loki_oauth2_allowed_groups

List of groups to allow access

#### Default value

```YAML
loki_oauth2_allowed_groups: []
```

#### Example usage

```YAML
loki_oauth2_allowed_groups:
  - /Group1
  - /Group2
  - /Group3
```

### loki_oauth2_client_id

Client ID for OAuth2 authentication

#### Default value

```YAML
loki_oauth2_client_id:
```

### loki_oauth2_client_secret

Client secret for OAuth2 authentication

#### Default value

```YAML
loki_oauth2_client_secret:
```

### loki_oauth2_cookie_secret

Cookie secret used by OAuth2 proxy

#### Default value

```YAML
loki_oauth2_cookie_secret:
```

### loki_oauth2_default_labels

List of default labels to assign to docker on OAuth2 Proxy

#### Default value

```YAML
loki_oauth2_default_labels: []
```

### loki_oauth2_default_publish

List of default port publishing for docker on OAuth2 Proxy

#### Default value

```YAML
loki_oauth2_default_publish: []
```

#### Example usage

```YAML
loki_oauth2_default_publish:
  - 127.0.0.1:3099:3099
```

### loki_oauth2_extra_labels

List of extra labels to assign to docker on OAuth2 Proxy

#### Default value

```YAML
loki_oauth2_extra_labels: []
```

### loki_oauth2_extra_publish

List of extra port publishing for docker on OAuth2 Proxy

#### Default value

```YAML
loki_oauth2_extra_publish: []
```

#### Example usage

```YAML
loki_oauth2_extra_publish:
  - 127.0.0.1:3099:3099
```

### loki_oauth2_image

#### Default value

```YAML
loki_oauth2_image: quay.io/oauth2-proxy/oauth2-proxy:v{{ loki_oauth2_version }}
```

### loki_oauth2_keycloak_url

URL of the Keycloak realm

#### Default value

```YAML
loki_oauth2_keycloak_url:
```

### loki_oauth2_listen_address

Listem address for the OAuth2 proxy

#### Default value

```YAML
loki_oauth2_listen_address: 0.0.0.0:3099
```

### loki_oauth2_network

#### Default value

```YAML
loki_oauth2_network: '{{ loki_network }}'
```

### loki_oauth2_provider

Provider for OAuth2 authentication

#### Default value

```YAML
loki_oauth2_provider: keycloak
```

### loki_oauth2_pull_image

#### Default value

```YAML
loki_oauth2_pull_image: true
```

### loki_oauth2_request_logging

Enable request logging for OAuth2 proxy

#### Default value

```YAML
loki_oauth2_request_logging: false
```

### loki_oauth2_static_groups

List of groups assigned to static users

#### Default value

```YAML
loki_oauth2_static_groups: []
```

### loki_oauth2_static_users

List of users to allow access

#### Default value

```YAML
loki_oauth2_static_users: []
```

#### Example usage

```YAML
loki_oauth2_static_users:
  - username: username1
    password: p455w0rd
  - username: username2
    password: p455w0rd
  - username: username3
    password: p455w0rd
```

### loki_oauth2_upstream

Upstream target for the OAuth2 proxy

#### Default value

```YAML
loki_oauth2_upstream: http://loki:3100
```

### loki_oauth2_version

Version of the OAuth2 Proxy to download

#### Default value

```YAML
loki_oauth2_version: 7.4.0
```

### loki_pull_image

Pull image as part of the tasks

#### Default value

```YAML
loki_pull_image: true
```

### loki_retention_time

Retention time to define the maximum age of the data

#### Default value

```YAML
loki_retention_time: 30d
```

### loki_version

Version of the release to install

#### Default value

```YAML
loki_version: 2.8.3
```

## Discovered Tags

**_loki_**

**_oauth2_**


## Dependencies

- [rolehippie.docker](https://github.com/rolehippie/docker)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
