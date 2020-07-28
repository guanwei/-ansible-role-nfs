# Ansible Role: NFS

Installs NFS utilities on RedHat/CentOS or Debian/Ubuntu.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
# example:
# nfs_exports:
#   - "/home/public   *(rw,sync,no_subtree_check,no_root_squash)"
nfs_exports: []
```

A list of exports which will be placed in the `/etc/exports` file. See Ubuntu's simple [Network File System (NFS)](https://help.ubuntu.com/lts/serverguide/network-file-system.html.en) guide for more info and examples. (Simple example: `nfs_exports: [ "/home/public   *(rw,sync,no_subtree_check,no_root_squash)" ]`).

## Dependencies

None.

## Example Playbook

requirements.yml
```
- name: nfs
  src: ssh://tfsemea1.ta.philips.com:22/tfs/TPC_Region27/CDI_PT/_git/ansible-role-nfs
  version: master
  scm: git
```

playbook.yml
```
- hosts: servers
  roles:
    - nfs
```
