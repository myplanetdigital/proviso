# Proviso
[![Build
Status](https://travis-ci.org/proviso/proviso.png)](https://travis-ci.org/proviso/proviso)

Proviso aims to be an SDK+API to provision platform-independent local
VMs for Drupal development. The project seeks to develop an extensible
framework and ecosystem for developers to achieve parity with multiple
production deployment targets, as well as a one-click installer control
panel that makes advanced local development accessible.

For more information, please check the [Wiki](https://github.com/proviso/proviso/wiki).

To participate, see [contributing](https://github.com/proviso/proviso/blob/master/CONTRIBUTING.md).

Pre-Requisites
--------------
- Git: http://git-scm.com/downloads
- Ruby: http://www.ruby-lang.org/en/downloads/
- RubyGems: http://rubygems.org/pages/download
- Rake: gem install rake
- Vagrant: http://downloads.vagrantup.com/

Usage
-----

### 1. Setup

    git clone https://github.com/proviso/proviso.git && cd proviso
    rake install_plugins

### 2a. Chef

    vagrant up

### 2b. Puppet

    [sudo] gem install librarian-puppet
    cd puppet && librarian-puppet install
    PROVISO_PROVISIONER=puppet vagrant up

When using Puppet, you'll need to preface every vagrant command with
`PROVISO_PROVISIONER=puppet`. To avoid having to type this for each
command, you may also export this environment variable for the remainder
of your terminal session by running:

    export PROVISO_PROVISIONER=puppet
