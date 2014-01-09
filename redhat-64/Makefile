NAME=sandbox
VERSION=current

all:

build:
	tar zcvf $(NAME)-$(VERSION).box Vagrantfile box.ovf box-disk1.vmdk

add:
	vagrant box add  $(NAME)-$(VERSION) $(NAME)-$(VERSION).box

clean:
	vagrant box remove $(NAME)-$(VERSION)
