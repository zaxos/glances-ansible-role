[![Build Status](https://travis-ci.org/zaxos/glances-ansible-role.svg?branch=master)](https://travis-ci.org/zaxos/glances-ansible-role)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-_zaxos.glances--ansible--role-blue.svg)](https://galaxy.ansible.com/zaxos/glances-ansible-role/)

glances-ansible-role
====================

Ansible role to install Glances.

Glances is a cross-platform monitoring tool which aims to present a maximum of information in a minimum of space through a curses or Web based interface. For more information see: https://github.com/nicolargo/glances

Requirements
------------
* centos/rhel 7  
* ansible >= 1.8

Installation
------------
```
$ ansible-galaxy install zaxos.glances-ansible-role
```

Example Playbook
----------------
```yaml
- hosts: servers
  vars:
    glances_version: 2.9.1
  roles:
    - role: zaxos.glances-ansible-role
```

Role Variables
--------------
Some variables that require review:
- `glances_version`: Glances version to be installed. Default is "2.9.1".
- `glances_state`: Default is "present". Set to "absent" for removal.
- `glances_optional_libraries`: Optional libraries to be installed in order to use optional features.  
Default is: `"action,batinfo,browser,cpuinfo,chart,docker,export,folders,gpu,ip,raid,snmp,web,wifi"`
