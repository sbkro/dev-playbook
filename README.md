# About
Ansible playbook for building my development enviroment.


# How to install

## OS X

After you have installed OS X, please run the following command.

### Testing (Remote install using vagrant + ansible)

```sh
$ cd <vagrant_dir>
$ vagrant init # create osx virtual machine.
$ vagrant up
$ git clone https://github.com/sbkro/dev-playbook.git
$ vagrant ssh-config --hosts osx > dev-playbook/playbook/ssh.config
$ cd dev-playbook/playbook
$ ansible-playbook -i hosts_remote osx.yml
```

### Production (Local install)

```sh
$ xcode-select --install # install command line tools from GUI.
$ sudo easy_install pip
$ sudo pip install ansible
$ git clone https://github.com/sbkro/dev-playbook.git
$ cd dev-playbook/playbook
$ ansible-playbook -i hosts_local osx.yml --connection=local -K
```

# Environments
* Host: OSX 10.11, Guest: OSX 10.11 (remote install)
* Host: OSX 10.11 (local install)

# TODO
* Add infrastructure test. (serverspec)
* Linux support.
