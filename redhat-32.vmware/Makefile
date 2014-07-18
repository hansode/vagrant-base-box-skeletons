NAME=redhat-32
PROVIDER=vmware_workstation

all:

build:
	tar zcvf $(NAME).$(PROVIDER).box Vagrantfile box-disk1.vmdk metadata.json box.vmsd box.vmx box.vmxf

add:
	vagrant box add $(NAME) $(NAME).$(PROVIDER).box

clean:
	vagrant box remove $(NAME) --provider $(PROVIDER)
