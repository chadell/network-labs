# Network Automation training

# Vagrant Lab Environment

```
+---------------+               +---------------+
|    routerA    |eth2       eth2|    routerB    |
|      VyOS     +---------------+      VyOS     |
| 192.168.0.100 |               | 192.168.0.101 |
+--------+------+               +-------+-------+
         | eth1                    eth1 |
         |      oob mgmt network        |
       +-+--------------+---------------+-+
                        |
                        |
                +-------+-------+
                |     mgmt      |
                |    Ubuntu     |
                | 192.168.0.200 |
                +---------------+
```

## Setup the environment

### Install VirtualBox

https://www.virtualbox.org/wiki/Downloads

### Install Vagrant

https://www.vagrantup.com/downloads.html

#### Install Vagrant plugins

```
$ vagrant plugin install vagrant-vyos
```

#### Run Vagrantfile

```
$ vagrant up
```

### Clean scenario

```
$ vagrant destroy
$ vagrant up
```

or clean the config on the VyOS routers:

```
$ vagrant ssh routerA
$ configure
# load /opt/vyatta/etc/config/config.boot
# commit
```
