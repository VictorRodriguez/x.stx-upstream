NAME ?= "horizon"
DEBMAKE ?= "python"
SRC_PATH ?= "../sources"
all:
	sudo apt-get source $(NAME)
	sudo rm -rf /var/cache/pbuilder/result/*.deb
	sudo pbuilder build --override-config *.dsc
	mkdir -p results/
	sudo cp -rf /var/cache/pbuilder/result/*.deb results/
	sudo cp results/*.deb /usr/local/mydebs/

clean:
	rm -rf results/
	rm -rf *.tar.gz
	sudo rm -rf $(NAME)-*/
	rm -rf *.deb
	rm -rf *.debian.tar.xz
	rm -rf *orig.tar.gz
	rm -rf *.changes
	rm -rf *.dsc
	rm -rf *.build
