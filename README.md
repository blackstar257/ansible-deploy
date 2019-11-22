# Ansible Role: deploy

[![Ansible Role](https://img.shields.io/badge/role-blackstar257.deploy-blue.svg)](https://galaxy.ansible.com/blackstar257/deploy/)
[![Build Status](https://travis-ci.com/blackstar257/ansible-deploy.svg?branch=master)](https://travis-ci.com/blackstar257/ansible-deploy)

Installs deployment private ssh key for GitHub on RHEL/CentOS or Debian/Ubuntu servers for the duration of the playbook. There is a handler to remove once finished.

## Requirements

None

## Role Variables

This needs to be a base64 encoded string of your private ssh key.

```yaml
ssh_private_key: Y29uZ3JhdHMgeW91IGRlY29kZWQgdGhpcyB0ZXh0IGhlcmVzIGEgY29va2llCg==
```

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  become: yes
  vars:
    ssh_private_key: Y29uZ3JhdHMgeW91IGRlY29kZWQgdGhpcyB0ZXh0IGhlcmVzIGEgY29va2llCg==
  roles:
    - blackstar257.deploy
```

## License

MIT

## Author Information

blackstar257
