.PHONY: clean-vm clean-vagrant-metadata

all: test

test: test-boot test-install

test-boot:
	vagrant up

test-install: test-boot
	vagrant ssh -c "cd /vagrant && clang++ -o hello hello.cpp && ./hello"

clean-vm:
	-vagrant destroy -f

clean-vagrant-metadata:
	-rm -rf .vagrant

clean: clean-vm clean-vagrant-metadata
