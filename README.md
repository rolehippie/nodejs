# nodejs

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/nodejs)
[![General Workflow](https://github.com/rolehippie/nodejs/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/nodejs/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/nodejs/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/nodejs/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/nodejs/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/nodejs/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/nodejs)](https://github.com/rolehippie/nodejs/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.nodejs-blue)](https://galaxy.ansible.com/rolehippie/nodejs)

Ansible role to install nodejs javascript runtime.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [nodejs_arch](#nodejs_arch)
  - [nodejs_keyring](#nodejs_keyring)
  - [nodejs_packages](#nodejs_packages)
  - [nodejs_version](#nodejs_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### nodejs_arch

Architecture for nodejs repo

#### Default value

```YAML
nodejs_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

### nodejs_keyring

Path for the repository keyring

#### Default value

```YAML
nodejs_keyring: /usr/share/keyrings/nodesource-archive-keyring.gpg
```

### nodejs_packages

List of packages to install

#### Default value

```YAML
nodejs_packages:
  - nodejs
```

### nodejs_version

Major version of nodejs to install

#### Default value

```YAML
nodejs_version: 18
```

## Discovered Tags

**_nodejs_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
