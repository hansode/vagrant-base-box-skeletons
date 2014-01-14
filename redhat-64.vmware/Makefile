NAME=redhat-64
PROVIDER=vmware_workstation

all:

build:
	tar zcvf $(NAME).$(PROVIDER).box Vagrantfile metadata.json $(NAME).vmdk $(NAME).vmsd $(NAME).vmx $(NAME).vmxf

add:
	vagrant box add $(NAME) $(NAME).$(PROVIDER).box

clean:
	vagrant box remove $(NAME) $(PROVIDER)
