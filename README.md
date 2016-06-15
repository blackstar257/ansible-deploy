# Ansible Role: deploy

[![Build Status](https://travis-ci.org/blackstar257/ansible-role-deploy.svg?branch=master)](https://travis-ci.org/blackstar257/ansible-role-deploy)
Installs deployment private ssh key on RHEL/CentOS or Debian/Ubuntu servers for the duration of the playbook. There is a handler to remove once finished.

## Requirements

No special requirements; note that this role requires root access, so either run it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

    - hosts: all
      roles:
        - role: blackstar257.deploy
          become: yes

## Role Variables

This needs to be a base64 encoded string of your private ssh key.

    github_private_key: None

## Dependencies

None.

## Example Playbook

    - hosts: db-servers
      become: yes
      vars_files:
        - vars/main.yml
      roles:
        - { role: blackstar257.deploy }

*Inside `vars/main.yml`*:

    github_private_key: AJSDFLJASDCKASDJFKASDJFASDF

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Kyle Umstatter](https://blackstar257.github.io/).
