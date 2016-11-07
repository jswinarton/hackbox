# pandora

A skeleton for building a generic, hackable Ubuntu 14.04 x64 VM using Vagrant. Requires VirtualBox and Ansible.

At minimum, this repo creates an Ubuntu Trusty VM using VirtualBox, makes some minor system modifications ([see the vagrant role](./provisiong/roles/vagrant)), and installs [hackbox-user](https://github.com/jswinarton/hackbox-user). This repo also contains a handful of roles for installing commonly used languages and utilities, such as Python, Ruby, Java, Erlang, Elixir, PostgreSQL, and more.


## Installation

Clone this repo. In `site.yml`, enable any of the scaffolding roles you want. Then:

```
ansible-galaxy install -r provisioning/requirements.yml  # run with -f to upgrade existing installs
vagrant up
```
