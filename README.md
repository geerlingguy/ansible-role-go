# Ansible Role: Go

[![CI](https://github.com/geerlingguy/ansible-role-go/workflows/CI/badge.svg?event=push)](https://github.com/geerlingguy/ansible-role-go/actions?query=workflow%3ACI)

An Ansible Role that installs Go (the language) on Linux.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    go_version: "1.17.3"
    go_platform: linux
    go_arch: amd64

Version, platform, and architecture to use when downloading Go.

    go_tarball: go{{ go_version }}.{{ go_platform }}-{{ go_arch }}.tar.gz
    go_download_url: https://dl.google.com/go/{{ go_tarball }}

These two variables are used to build the download URL when installing Go.

    go_checksum: '550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'

SHA256 checksum of the Go download. If changing the version, platform, or architecture, you will also need to update this checksum, too.

## Dependencies

None.

## Example Playbook

    - hosts: myserver
      roles:
        - { role: geerlingguy.go }

## License

MIT / BSD

## Author Information

This role was created in 2021 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
