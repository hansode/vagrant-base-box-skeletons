NAME=redhat-64
PROVIDER=virtualbox

all:

build:
	tar zcvf $(NAME).$(PROVIDER).box Vagrantfile box.ovf box-disk1.vmdk

add:
	vagrant box add $(NAME) $(NAME).$(PROVIDER).box

clean:
	vagrant box remove $(NAME) $(PROVIDER)
