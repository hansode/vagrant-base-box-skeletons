NAME=redhat-64_vmware

all:

build:
	tar zcvf $(NAME).box Vagrantfile metadata.json $(NAME).vmdk $(NAME).vmsd $(NAME).vmx $(NAME).vmxf

add:
	vagrant box add  $(NAME) $(NAME).box

clean:
	vagrant box remove $(NAME)
