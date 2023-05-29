include ./CONFIG
DEPENDS=
PACKAGE_DIR?=${PWD}

all:
	$(SUDO) $(MAKE) mrproper
	mkdir -p data root/var/jb/usr/bin
	cp -f ../../fsmon-ios root/var/jb/usr/bin/fsmon
	chmod +x root/var/jb/usr/bin/fsmon
	mkdir -p root/var/jb/usr/share/man/man1
	cp -f ../../fsmon.1 root/var/jb/usr/share/man/man1/fsmon.1
	$(SUDO) $(MAKE) debroot

clean:
	$(SUDO) $(MAKE) deb_clean

mrproper: clean
	rm -rf root

include deb.mk
