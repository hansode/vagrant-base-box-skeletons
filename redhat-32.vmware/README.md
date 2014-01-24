redhat-32.vmware
================

Requirements
------------

+ [Vagrant](http://www.vagrantup.com/)
+ Windows
  + [VMware Workstation](http://www.vmware.com/jp/products/workstation/)
  + [vagrant-vmware-workstation](http://docs.vagrantup.com/v2/vmware/installation.html)
+ Mac
  + [VMware Fusion](http://www.vmware.com/jp/products/fusion/)
  + [vagrant-vmware-fusion](http://docs.vagrantup.com/v2/vmware/installation.html)

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
$ cp /path/to/box-disk1.vmdk ./box-disk1.vmdk
```

Building box file

```
$ make build
tar zcvf redhat-32.vmware_workstation.box Vagrantfile box-disk1.vmdk metadata.json box.vmsd box.vmx box.vmxf
Vagrantfile
box-disk1.vmdk
metadata.json
box.vmsd
box.vmx
box.vmxf
```

Adding the generated box

```
$ make add
vagrant box add redhat-32 redhat-32.vmware_workstation.box
Downloading box from URL: file:C:\cygwin\home\hansode\work\repos\git\github.com\vagrant-base-box-skeletons\redhat-32.vmware\redhat-32.vmware_workstation.box
Extracting box...ate: 252M/s, Estimated time remaining: --:--:--)
Successfully added box 'redhat-32' with provider 'vmware_workstation'!
```
