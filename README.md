# Ansible Role: Installs Java 11 Open JDK

Easy way of Java 11 Open JDK installation on Linux. Supports remote download, local download of official package, symlinking to lastest folder, alternatives settings.

Travis status:   [![Build Status](https://travis-ci.org/KAMI911/ansible-role-java-open-jdk11.svg?branch=master)](https://travis-ci.org/KAMI911/ansible-role-java-open-jdk11)
Code Climate status: [![Code Climate](https://codeclimate.com/github/KAMI911/ansible-role-java-open-jdk11/badges/gpa.svg)](https://codeclimate.com/github/KAMI911/ansible-role-java-open-jdk11)
Test Coverage status: [![Test Coverage](https://codeclimate.com/github/KAMI911/ansible-role-java-open-jdk11/badges/coverage.svg)](https://codeclimate.com/github/KAMI911/ansible-role-java-open-jdk11/coverage)

## Table of Contents

1. [Requirements][Requirements]
2. [Installation][Installation]
3. [Role Variables][Role Variables]
4. [Dependencies][Dependencies]
5. [Example Playbook][Example Playbook]
6. [Licensing][Licensing]
7. [Author Information][Author Information]
8. [Support][Support]
9. [Contributing][Contributing]
10. [Donation][Donation]

## Requirements

None.

## Installation

    ansible-galaxy install kami911.java-open-jdk11

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    force_java_install: False

Force to install Java on already installed system.

    java_installer_force_overwrite: False

Force to overwrite Java installer.

    java_installer_keep: False

Do not delete Java installer.

    java_installer_local: False

Install local (form Ansible host) JDK/Server JRE instead of downloading on target machine.

    java_type: jdk

Type of Java installer - JDK is: jdk, and Server JRE is: serverjre

    java_version: 11

Java major version.

    java_update: 0

Java minor version.

    java_build: "10"

Java micro version.

    java_platform: linux-x64

Java platform to install.

    java_bins: [ 'javah', 'javap', 'jmap', 'extcheck', 'pack200', 'jrunscript', 'jinfo', 'jcontrol', 'jmc', 'keytool', 'schemagen', 'jjs', 'jvisualvm', 'policytool', 'rmid', 'wsgen', 'javaws', 'javadoc

Update alternatives on these binaries.

    java_bins_priority: 9

Alternatives priority on these binaries.

    java_usr_folder: /usr/java

Location of installed Java home.

    java_latest_folder: /usr/java/latest

Where to link the latest folder.

    java_download_base_url: https://download.java.net/java/ga/

Download link of Java installers.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - java-open-jdk11

## Licensing

The lactransformer application and documantations are licensed under the terms of
the MIT / BSD, you will find a copy of this license in the
[LICENSE](LICENSE) file included in the source package.

## Author Information

This role was created in 2016-2019 by Kálmán Szalai - KAMI

## Support

If you have any question, do not hesitate and drop me a line.
If you found a bug, or have a feature request, you can [fill an issue](https://github.com/KAMI911/ansible-role-java-open-jdk11/issues).

### Using as a submudule of an AWX playbook

#### Add as a submodule

```
git submodule add --force git@github.com:KAMI911/ansible-role-java-open-jdk11.git roles/java-open-jdk11
```

#### Update as sumodule

Update only this submodule

```
git submodule update --remote roles/java-open-jdk11/
```

Update all submodules:

```
git submodule foreach git pull origin master
```

## Contributing

There are many ways to contribute to ansible-role-java-open-jdk11 -- whether it be sending patches,
testing, reporting bugs, or reviewing and updating the documentation. Every
contribution is appreciated!

Please continue reading in the [contributing chapter](CONTRIBUTING.md).

### Fork me on Github

SSH:

    git@github.com:KAMI911/ansible-role-java-open-jdk11.git

HTTPS:

    https://github.com/KAMI911/ansible-role-java-open-jdk11

Add a new remote `upstream` with this repository as value.

```
git remote add upstream https://github.com/KAMI911/ansible-role-java-open-jdk11.git
```

You can pull updates to your fork's master branch:

```
git fetch --all
git pull upstream HEAD
```

## Donation

If you find this useful, please consider a donation:

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RLQZ58B26XSLA)

<!-- TOC URLs -->
[Requirements]: #requirements
[Installation]: #installation
[Role Variables]: #role_variables
[Dependencies]: #dependencies
[Example Playbook]: #example_playbook
[Licensing]: #licensing
[Author Information]: #author_information
[Support]: #support
[Contributing]: #contributing
[Donation]: #donation

