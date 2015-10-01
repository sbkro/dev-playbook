# About
Ansible playbook for building my development enviroment.


# How to install

## OS X

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
$ ansible-playbook -i hosts osx.yml --connection=local -K
```

If you run the ansible playbook to OSX 10.11, you have disable "rootless" temporarily.

Beta version is as follow.

```sh
# disable rootless.
$ sudo nvram boot-args="rootless=0"
$ sudo reboot

# enable rootless.
$ sudo nvram boot-args="rootless=1"
```

GM Candidate and Official version are as follows. This command must run in terminal of recovery mode.

```sh
# disalble rootless.
$ csrutil disable

# enable rootless.
$ csrutil enable
```


# Environments
* Host: OSX 10.9  (local install)
* Host: OSX 10.10 (local install)
* Host: OSX 10.11 (local install)
* Host: OSX 10.9, Guest: OSX 10.9 (remote install)


# TODO
* Add infrastructure test. (serverspec)
* Linux support.
