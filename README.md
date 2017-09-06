# ansible-role-vagrant-ruby-dev [![Build Status][travis.svg]][travis]

An Ansible role for a Vagrant-based Ruby development setup.

Available on Ansible Galaxy at [`naftulikay.vagrant-ruby-dev`][galaxy].

## Requirements

A Vagrant machine running a supported operating system.

## Role Variables

<dl>
  <dt><code>ruby_version</code></dt>
  <dd>The version of Ruby to install.</dd>
  <dt><code>vagrant_user</code></dt>
  <dd>The username of the Vagrant user, defaults to <code>vagrant</code></dd>
</dl>

> Please see the upstream [`naftulikay.vagrant-base`][vagrant-base] and [`naftulikay.ruby-dev`][ruby-dev] roles for
additional supported variables.

## Dependencies

 - [`naftulikay.vagrant-base`][vagrant-base]: Provides base Vagrant configuration.
 - [`naftulikay.ruby-dev`][ruby-dev]: Provides a basic Ruby development environment.

## Example Playbook

Install a Ruby development environment within the Vagrant machine:

```
---
- hosts: all
  roles:
    - role: vagrant-ruby-dev
      ruby_version: 2.4.1
```

## LICENSE

MIT.

 [travis]: https://travis-ci.org/naftulikay/ansible-role-vagrant-ruby-dev
 [travis.svg]: https://travis-ci.org/naftulikay/ansible-role-vagrant-ruby-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/vagrant-ruby-dev/
 [vagrant-base]: https://galaxy.ansible.com/naftulikay/vagrant-base/
 [ruby-dev]: https://galaxy.ansible.com/naftulikay/ruby-dev/
