# About

This repository contains ansible role for Jenkins slave setup. Molecule is used to perform testing of ansible role in docker image with Testinfra. Supported OS:

* Ubuntu/Debian
* RedHat/CentOS
* Amazon Linux AMI

# Requirements

* gcc
* pip
* virtualenv
* molecule
* ansible
* docker

# Usage

* Put Jenkins master key in files folder named as id_rsa.pub

* Make sure you have gcc installed in the system. Install pip in your system then install virtualenv globally. Then create python environment in the project root as following,

```
$ virtualenv --python=/usr/bin/python .venv
```

Use environment python and then install other dependencies,

```
$ source .venv/bin/activate
$ pip install ansible
$ pip install molecule
$ pip install docker
```

In the project root directory run the following command to run tests,

```
$ molecule test
```

If your docker image and role is the same but test case changes then use,

```
$ molecule create
$ molecule Converge
$ molecule verify
```
