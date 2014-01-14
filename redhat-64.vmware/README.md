redhat-64_vmware
================

Requirements
------------

+ Vagrant
+ VMware Workstation

Usage
-----

```
$ make build
$ make add
$ make clean
```

Getting Started
---------------

Pre-setup vmdk file

```
$ cp /path/to/box-disk1.vmdk redhat-64_vmware.vmdk
```

Building box file

```
$ make build
$ make build
tar zcvf redhat-64.vmware_workstation.box Vagrantfile box-disk1.vmdk metadata.json box.vmsd box.vmx box.vmxf
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
vagrant box add redhat-64 redhat-64.vmware_workstation.box
Downloading box from URL: file:C:\cygwin\home\hansode\work\repos\git\github.com\vagrant-base-box-skeletons\redhat-64.vmware\redhat-64.vmware_workstation.box
Extracting box...ate: 252M/s, Estimated time remaining: --:--:--)
Successfully added box 'redhat-64' with provider 'vmware_workstation'!
```
