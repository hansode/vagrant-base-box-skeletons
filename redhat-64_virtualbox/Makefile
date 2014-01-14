NAME=redhat-64

all:

build:
	tar zcvf $(NAME).box Vagrantfile box.ovf box-disk1.vmdk

add:
	vagrant box add  $(NAME) $(NAME).box

clean:
	vagrant box remove $(NAME)
