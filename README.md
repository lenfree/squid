Rev-proxy:
==============

This is to quickly setup squid.

Getting Started:
---------------

```
$ pip install ansible or brew install ansible for OSX
$ git clone git@github.com:lenfree/squid.git
$ cd squid
$ ansible-playbook -i inventory hosts proxy.yml -k -K -u <username>
```

Using Vagrant:
--------------

```
$ vagrant up
```
