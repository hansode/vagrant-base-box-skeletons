NAME=redhat-32
PROVIDER=virtualbox

all:

build:
	tar zcvf $(NAME).$(PROVIDER).box Vagrantfile box-disk1.vmdk box.ovf

add:
	vagrant box add $(NAME) $(NAME).$(PROVIDER).box

clean:
	vagrant box remove $(NAME) --provider $(PROVIDER)
