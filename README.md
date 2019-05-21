![Logo](https://raw.githubusercontent.com/idealista/zanata_role/master/logo.gif)

# Zanata Ansible Role 
[![Build Status](https://travis-ci.org/idealista/zanata_role.png)](https://travis-ci.org/idealista/zanata_role)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-idealista.zanata__role-B62682.svg)](https://galaxy.ansible.com/idealista/zanata_role)

This Ansible role installs a Zanata server in a Debian environment. Based on the instructions present in [Zanata Platform Documentation](http://docs.zanata.org/en/latest/user-guide/system-admin/configuration/installation/).

- [Getting Started](#getting-started)
    - [Prerequisities](#prerequisities)
    - [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)

## Getting Started

These instructions will get you a copy of the role for your Ansible Playbook. Once launched, it will install a [Zanata](http://docs.zanata.org/en/latest/user-guide/system-admin/configuration/installation/) server in a Debian system.

### Prerequisities

Ansible 2.4.1.0 version installed.
Inventory destination should be a Debian environment.

> :warning: This role asumes that [Java](https://github.com/idealista/java_role), [WildFly](https://github.com/idealista/wildfly-role) and [MySQL](https://github.com/idealista/mysql_role) are previously installed. 

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Vagrant](https://www.vagrantup.com/) as driver (with [vagrant-hostmanager](https://github.com/devopsgroup-io/vagrant-hostmanager) plugin) and [VirtualBox](https://www.virtualbox.org/) as provider. Docker could be used as driver too.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: idealista/zanata_role
  version: 1.1.0
  name: zanata
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
---
- hosts: someserver
  roles:
    - { role: zanata }
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties.

## Testing

Execute `$ molecule test` under zanata_role folder to run the automated tests suite.

## Built With

![Ansible](https://img.shields.io/badge/ansible-2.4.1.0-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/zanata_role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/zanata_role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.
