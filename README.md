# Ansible Role: apt-sources

[![Build Status](https://travis-ci.org/bramford/ansible-role-apt-sources.svg?branch=master)](https://travis-ci.org/bramford/ansible-role-apt-sources)

Ansible role that configures apt sources for Ubuntu and Debian. Defaults to the dynamic mirrors


## Supported Operating Systems

- Debian (all versions)
- Ubuntu (all versions)

## Requirements

- Ansible 2.1+

## Role Variables

See `./defaults/main.yml` for configurable variables and their defaults

## Example playbook

    ---
    - name: Example play
      hosts: all
      roles:
        - { apt-sources }

## Example playbook (with some optional vars set)

    ---
    - name: Example play with optional vars set
      hosts: all
      roles:
        - { apt-sources,
            apt_sources_file: "/etc/apt/sources.list.d/mysource.list",
            apt_sources_security: no
          }

## Add as a submodule to your playbook repo

    git submodule add https://github.com/bramford/ansible-role-apt-sources.git roles/apt-sources
