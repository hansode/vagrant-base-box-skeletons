NAME=redhat-64_vmware
VERSION=current

all:

build:
	tar zcvf $(NAME)-$(VERSION).box Vagrantfile metadata.json $(NAME).vmdk $(NAME).vmsd $(NAME).vmx $(NAME).vmxf

add:
	vagrant box add  $(NAME)-$(VERSION) $(NAME)-$(VERSION).box

clean:
	vagrant box remove $(NAME)-$(VERSION)
