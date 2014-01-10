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
tar zcvf redhat-64_vmware-current.box Vagrantfile metadata.json redhat-64_vmware.vmdk redhat-64_vmware.vmsd redhat-64_vmware.vmx redhat-64_vmware.vmxf
Vagrantfile
metadata.json
redhat-64_vmware.vmdk
redhat-64_vmware.vmsd
redhat-64_vmware.vmx
redhat-64_vmware.vmxf
```

Adding the generated box

```
$ make add
vagrant box add  redhat-64_vmware-current redhat-64_vmware-current.box
Downloading box from URL: file:C:\cygwin\home\hansode\work\repos\git\github.com\vagrantfiles\redhat-64_vmware\redhat-64_vmware-current.box
Extracting box...ate: 600M/s, Estimated time remaining: --:--:--)
Successfully added box 'redhat-64_vmware-current' with provider 'vmware_workstation'!
```
