# Ansible Role: erigon

### Description

Ansible role that will install, configure and runs Erigon

### Table of Contents

- [Supported Platforms](#supported-platforms)
- [Dependencies](#dependencies)
- [Role Variables](#role-variables)
- [Example Playbook](#example-playbook)
- [License](#license)
- [Author Information](#author-information)

### Supported Platforms

```
* Debian
* Ubuntu
* Redhat(CentOS/Fedora)
* Amazon
```

### Dependencies

- Go 1.13.x or greater

### Role Variables:

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file. By and large these variables are configuration options. 

### Example Playbook

1. **Install role from Ansible Galaxy**

`ansible-galaxy install consensys.erigon`

**Create the `requirements.yml` with required variables**

```yaml
- hosts: localhost
  connection: local
  force_handlers: True

  roles:
    - role: consensys.erigon
      vars:
        erigon_version: vX.Y.Z

```

2. **Install role from Github**

`ansible-galaxy install git+https://github.com/consensys/ansible-role-erigon.git`

**Create `requirements.yml` for Github installed role**

```yaml
- hosts: localhost
  connection: local
  force_handlers: True

  roles:
    - role: ansible-role-erigon
      vars:
        erigon_version: vX.Y.Z

```

Run the result with the following: `ansible-playbook -v requirements.yml -vvv`

### License

Apache

### Author Information

Consensys, 2022
