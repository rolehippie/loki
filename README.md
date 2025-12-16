# loki

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/loki)
[![General Workflow](https://github.com/rolehippie/loki/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/loki/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/loki/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/loki/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/loki/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/loki/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/loki)](https://github.com/rolehippie/loki/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.loki-blue)](https://galaxy.ansible.com/rolehippie/loki)

Ansible role to install and configure loki.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of contents

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [loki_additional_config](#loki_additional_config)
  - [loki_auth_enabled](#loki_auth_enabled)
  - [loki_chunk_store_config](#loki_chunk_store_config)
  - [loki_combined_config](#loki_combined_config)
  - [loki_common_config](#loki_common_config)
  - [loki_compactor_config](#loki_compactor_config)
  - [loki_cpu_shares](#loki_cpu_shares)
  - [loki_default_folders](#loki_default_folders)
  - [loki_default_labels](#loki_default_labels)
  - [loki_default_publish](#loki_default_publish)
  - [loki_default_volumes](#loki_default_volumes)
  - [loki_distributor_config](#loki_distributor_config)
  - [loki_domain](#loki_domain)
  - [loki_extra_folders](#loki_extra_folders)
  - [loki_extra_labels](#loki_extra_labels)
  - [loki_extra_publish](#loki_extra_publish)
  - [loki_extra_volumes](#loki_extra_volumes)
  - [loki_frontend_worker_config](#loki_frontend_worker_config)
  - [loki_grpc_server_max_recv_msg_size](#loki_grpc_server_max_recv_msg_size)
  - [loki_grpc_server_max_send_msg_size](#loki_grpc_server_max_send_msg_size)
  - [loki_image](#loki_image)
  - [loki_index_gateway_config](#loki_index_gateway_config)
  - [loki_ingester_client_config](#loki_ingester_client_config)
  - [loki_ingester_config](#loki_ingester_config)
  - [loki_limits_config](#loki_limits_config)
  - [loki_max_global_streams_per_user](#loki_max_global_streams_per_user)
  - [loki_max_streams_per_user](#loki_max_streams_per_user)
  - [loki_memberlist_config](#loki_memberlist_config)
  - [loki_memory_limit](#loki_memory_limit)
  - [loki_memory_soft_limit](#loki_memory_soft_limit)
  - [loki_memory_swap](#loki_memory_swap)
  - [loki_network](#loki_network)
  - [loki_number_of_cpus](#loki_number_of_cpus)
  - [loki_oauth2_access_logging](#loki_oauth2_access_logging)
  - [loki_oauth2_allowed_groups](#loki_oauth2_allowed_groups)
  - [loki_oauth2_client_id](#loki_oauth2_client_id)
  - [loki_oauth2_client_secret](#loki_oauth2_client_secret)
  - [loki_oauth2_cookie_secret](#loki_oauth2_cookie_secret)
  - [loki_oauth2_cpu_shares](#loki_oauth2_cpu_shares)
  - [loki_oauth2_default_labels](#loki_oauth2_default_labels)
  - [loki_oauth2_default_publish](#loki_oauth2_default_publish)
  - [loki_oauth2_enabled](#loki_oauth2_enabled)
  - [loki_oauth2_extra_labels](#loki_oauth2_extra_labels)
  - [loki_oauth2_extra_publish](#loki_oauth2_extra_publish)
  - [loki_oauth2_image](#loki_oauth2_image)
  - [loki_oauth2_keycloak_url](#loki_oauth2_keycloak_url)
  - [loki_oauth2_listen_address](#loki_oauth2_listen_address)
  - [loki_oauth2_memory_limit](#loki_oauth2_memory_limit)
  - [loki_oauth2_memory_soft_limit](#loki_oauth2_memory_soft_limit)
  - [loki_oauth2_memory_swap](#loki_oauth2_memory_swap)
  - [loki_oauth2_network](#loki_oauth2_network)
  - [loki_oauth2_number_of_cpus](#loki_oauth2_number_of_cpus)
  - [loki_oauth2_provider](#loki_oauth2_provider)
  - [loki_oauth2_pull_image](#loki_oauth2_pull_image)
  - [loki_oauth2_request_logging](#loki_oauth2_request_logging)
  - [loki_oauth2_static_groups](#loki_oauth2_static_groups)
  - [loki_oauth2_static_users](#loki_oauth2_static_users)
  - [loki_oauth2_upstream](#loki_oauth2_upstream)
  - [loki_oauth2_version](#loki_oauth2_version)
  - [loki_pattern_ingester_config](#loki_pattern_ingester_config)
  - [loki_pull_image](#loki_pull_image)
  - [loki_querier_config](#loki_querier_config)
  - [loki_query_scheduler_config](#loki_query_scheduler_config)
  - [loki_retention_time](#loki_retention_time)
  - [loki_ruler_config](#loki_ruler_config)
  - [loki_ruler_storage_config](#loki_ruler_storage_config)
  - [loki_schema_config](#loki_schema_config)
  - [loki_server_config](#loki_server_config)
  - [loki_storage_config](#loki_storage_config)
  - [loki_table_manager_config](#loki_table_manager_config)
  - [loki_ui_config](#loki_ui_config)
  - [loki_version](#loki_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### loki_additional_config

Additional optional config to append

#### Default value

```YAML
loki_additional_config:
```

### loki_auth_enabled

Enable authentication for Loki

#### Default value

```YAML
loki_auth_enabled: false
```

### loki_chunk_store_config

Configuration block for chunk_store_config

#### Default value

```YAML
loki_chunk_store_config:
```

### loki_combined_config

Final combined config writte to file

#### Default value

```YAML
loki_combined_config: |
  auth_enabled: {{ loki_auth_enabled | lower }}
  {% if loki_server_config | length > 0 %}

  server:
    {{ loki_server_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_ui_config | length > 0 %}

  ui:
    {{ loki_ui_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_distributor_config | length > 0 %}

  distributor:
    {{ loki_distributor_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_querier_config | length > 0 %}

  querier:
    {{ loki_querier_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_query_scheduler_config | length > 0 %}

  query_scheduler:
    {{ loki_query_scheduler_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_ruler_config | length > 0 %}

  ruler:
    {{ loki_ruler_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_ruler_storage_config | length > 0 %}

  ruler_storage:
    {{ loki_ruler_storage_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_ingester_client_config | length > 0 %}

  ingester_client:
    {{ loki_ingester_client_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_ingester_config | length > 0 %}

  ingester:
    {{ loki_ingester_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_pattern_ingester_config | length > 0 %}

  pattern_ingester:
    {{ loki_pattern_ingester_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_index_gateway_config | length > 0 %}

  index_gateway:
    {{ loki_index_gateway_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_storage_config | length > 0 %}

  storage_config:
    {{ loki_storage_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_chunk_store_config | length > 0 %}

  chunk_store_config:
    {{ loki_chunk_store_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_schema_config | length > 0 %}

  schema_config:
    {{ loki_schema_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_compactor_config | length > 0 %}

  compactor_config:
    {{ loki_compactor_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_limits_config | length > 0 %}

  limits_config:
    {{ loki_limits_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_frontend_worker_config | length > 0 %}

  frontend_worker_config:
    {{ loki_frontend_worker_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_table_manager_config | length > 0 %}

  table_manager:
    {{ loki_table_manager_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_memberlist_config | length > 0 %}

  memberlist:
    {{ loki_memberlist_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_common_config | length > 0 %}

  common:
    {{ loki_common_config | from_yaml | to_nice_yaml(indent=2) | indent(width=2) | trim }}
  {% endif %}
  {% if loki_additional_config | length > 0 %}

  {{ loki_additional_config | from_yaml | to_nice_yaml(indent=2) | trim }}
  {% endif %}
```

### loki_common_config

Configuration block for common

#### Default value

```YAML
loki_common_config: |
  path_prefix: /loki
  replication_factor: 1

  ring:
    kvstore:
      store: inmemory
```

### loki_compactor_config

Configuration block for compactor

#### Default value

```YAML
loki_compactor_config:
```

### loki_cpu_shares

CPU shares with Docker deployment

#### Default value

```YAML
loki_cpu_shares:
```

#### Example usage

```YAML
loki_cpu_shares: '512'
```

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

### loki_distributor_config

Configuration block for distributor

#### Default value

```YAML
loki_distributor_config:
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

### loki_frontend_worker_config

Configuration block for frontend_worker

#### Default value

```YAML
loki_frontend_worker_config:
```

### loki_grpc_server_max_recv_msg_size

Limit on the size of a gRPC message can receive

#### Default value

```YAML
loki_grpc_server_max_recv_msg_size: 4194304
```

### loki_grpc_server_max_send_msg_size

Limit on the size of a gRPC message can send

#### Default value

```YAML
loki_grpc_server_max_send_msg_size: 4194304
```

### loki_image

Docker image to use for deployment on OAuth2 Proxy

#### Default value

```YAML
loki_image: grafana/loki:{{ loki_version }}
```

### loki_index_gateway_config

Configuration block for index_gateway

#### Default value

```YAML
loki_index_gateway_config:
```

### loki_ingester_client_config

Configuration block for ingester_client

#### Default value

```YAML
loki_ingester_client_config:
```

### loki_ingester_config

Configuration block for ingester

#### Default value

```YAML
loki_ingester_config:
```

### loki_limits_config

Configuration block for limits

#### Default value

```YAML
loki_limits_config: |
  max_streams_per_user: {{ loki_max_streams_per_user }}
  max_global_streams_per_user: {{ loki_max_global_streams_per_user }}
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

### loki_memberlist_config

Configuration block for memberlist

#### Default value

```YAML
loki_memberlist_config:
```

### loki_memory_limit

Memory limit with Docker deployment

#### Default value

```YAML
loki_memory_limit:
```

#### Example usage

```YAML
loki_memory_limit: 1024m
```

### loki_memory_soft_limit

Soft memory limit with Docker deployment

#### Default value

```YAML
loki_memory_soft_limit:
```

#### Example usage

```YAML
loki_memory_soft_limit: 512m
```

### loki_memory_swap

Swap usage with Docker deployment

#### Default value

```YAML
loki_memory_swap:
```

#### Example usage

```YAML
loki_memory_swap: 2048m
```

### loki_network

Optional docker network to attach on OAuth2 Proxy

#### Default value

```YAML
loki_network:
```

### loki_number_of_cpus

Number of CPUs with Docker deployment

#### Default value

```YAML
loki_number_of_cpus:
```

#### Example usage

```YAML
loki_number_of_cpus: '1.0'
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

### loki_oauth2_cpu_shares

CPU shares with Docker deployment

#### Default value

```YAML
loki_oauth2_cpu_shares:
```

#### Example usage

```YAML
loki_oauth2_cpu_shares: '512'
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

### loki_oauth2_enabled

Enable authentication for Loki

#### Default value

```YAML
loki_oauth2_enabled: false
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

### loki_oauth2_memory_limit

Memory limit with Docker deployment

#### Default value

```YAML
loki_oauth2_memory_limit:
```

#### Example usage

```YAML
loki_oauth2_memory_limit: 1024m
```

### loki_oauth2_memory_soft_limit

Soft memory limit with Docker deployment

#### Default value

```YAML
loki_oauth2_memory_soft_limit:
```

#### Example usage

```YAML
loki_oauth2_memory_soft_limit: 512m
```

### loki_oauth2_memory_swap

Swap usage with Docker deployment

#### Default value

```YAML
loki_oauth2_memory_swap:
```

#### Example usage

```YAML
loki_oauth2_memory_swap: 2048m
```

### loki_oauth2_network

#### Default value

```YAML
loki_oauth2_network: '{{ loki_network }}'
```

### loki_oauth2_number_of_cpus

Number of CPUs with Docker deployment

#### Default value

```YAML
loki_oauth2_number_of_cpus:
```

#### Example usage

```YAML
loki_oauth2_number_of_cpus: '1.0'
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
loki_oauth2_version: 7.13.0
```

### loki_pattern_ingester_config

Configuration block for pattern_ingester

#### Default value

```YAML
loki_pattern_ingester_config:
```

### loki_pull_image

Pull image as part of the tasks

#### Default value

```YAML
loki_pull_image: true
```

### loki_querier_config

Configuration block for querier

#### Default value

```YAML
loki_querier_config:
```

### loki_query_scheduler_config

Configuration block for query_scheduler

#### Default value

```YAML
loki_query_scheduler_config:
```

### loki_retention_time

Retention time to define the maximum age of the data

#### Default value

```YAML
loki_retention_time: 30d
```

### loki_ruler_config

Configuration block for ruler

#### Default value

```YAML
loki_ruler_config:
```

### loki_ruler_storage_config

Configuration block for ruler_storage

#### Default value

```YAML
loki_ruler_storage_config: |
  backend: local
  local:
    directory: /loki/rules
```

### loki_schema_config

Configuration block for schema_config

#### Default value

```YAML
loki_schema_config: |
  configs:
    - from: 2020-10-24
      store: boltdb-shipper
      object_store: filesystem
      schema: v13
      index:
        prefix: index_
        period: 24h
```

### loki_server_config

Configuration block for server

#### Default value

```YAML
loki_server_config: |
  http_listen_port: 3100
  grpc_server_max_recv_msg_size: {{ loki_grpc_server_max_recv_msg_size }}
  grpc_server_max_send_msg_size: {{ loki_grpc_server_max_send_msg_size }}
```

### loki_storage_config

Configuration block for storage_config

#### Default value

```YAML
loki_storage_config: |
  filesystem:
    directory: /loki/chunks
```

### loki_table_manager_config

Configuration block for table_manager

#### Default value

```YAML
loki_table_manager_config: |
  retention_deletes_enabled: {{ "true" if loki_retention_time | length > 0 else "false" }}
  retention_period: {{ loki_retention_time }}
```

### loki_ui_config

Configuration block for ui

#### Default value

```YAML
loki_ui_config:
```

### loki_version

Version of the release to install

#### Default value

```YAML
loki_version: 3.6.3
```

## Discovered Tags

**_loki_**

**_oauth2_**

## Dependencies

- [rolehippie.docker](https://github.com/rolehippie/docker)
- [community.general](https://github.com/ansible-collections/community.general)
- [community.docker](https://github.com/ansible-collections/community.docker)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
