# About
Ansible playbook for building my development enviroment.


# How to install

After you have installed OS X, please run the following command.

```sh
$ xcode-select --install
# install command line tools from GUI.
$ sudo easy_install pip
$ sudo pip install ansible
$ git clone https://github.com/sbkro/dev-playbook.git
$ cd dev-playbook/playbook
$ vi hosts
# edit host name
$ ansible-playbook -i hosts osx.yml --connection=local
```

# Environments
* Host: OSX 10.9 (local install)
* Host: OSX 10.9, Guest: OSX 10.9 (remote install)


# TODO
* Add enviroment test. (serverspec)
* Linux support.
