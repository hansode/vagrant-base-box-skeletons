redhat-64.virtualbox
====================

Requirements
------------

+ [Vagrant](http://www.vagrantup.com/)
+ [VirtualBox](https://www.virtualbox.org/)

Usage
-----

### Basic Vagrant Box Workflow

```
$ make build
$ make add
$ make clean
```

### Custom Vagrant Box Workflow

```
$ make build NAME=foo
$ make add   NAME=foo
$ make clean NAME=foo
```

Getting Started
---------------

Pre-setup vmdk file

```
$ cp /path/to/box-disk1.vmdk box-disk1.vmdk
```

Building box file

```
$ make build
tar zcvf redhat-64.virtualbox.box Vagrantfile box-disk1.vmdk box.ovf
Vagrantfile
box-disk1.vmdk
box.ovf
```

Adding the generated box

```
$ make clean add
vagrant box remove redhat-64 virtualbox
Removing box 'redhat-64' with provider 'virtualbox'...
vagrant box add redhat-64 redhat-64.virtualbox.box
Downloading box from URL: file:C:\cygwin\home\hansode\work\repos\git\github.com\vagrant-base-box-skeletons\redhat-64.virtualbox\redhat-64.virtualbox.box
Extracting box...ate: 229M/s, Estimated time remaining: --:--:--)
Successfully added box 'redhat-64' with provider 'virtualbox'!
```
