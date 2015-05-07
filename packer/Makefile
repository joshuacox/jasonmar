all: help

help:
	@echo ""
	@echo "-- Help Menu"
	@echo ""  Makes an image with chef in it
	@echo ""   1. make vbox       - your site will be in ../builds

qemu: buildqemu beep

qemudebug: buildqemudebug beep

vbox: buildvbox beep

vboxdebug: buildvboxdebug beep

buildqemudebug:
	/usr/bin/time -v packer build -debug --only=qemu jasonmar-debian-8.0-amd64.json

buildqemu:
	/usr/bin/time -v packer build --only=qemu jasonmar-debian-8.0-amd64.json

buildvboxdebug:
	/usr/bin/time -v packer build -debug --only=virtualbox-iso jasonmar-debian-8.0-amd64.json

buildvbox:
	/usr/bin/time -v packer build --only=virtualbox-iso jasonmar-debian-8.0-amd64.json

build7qemudebug:
	/usr/bin/time -v packer build -debug --only=qemu jasonmar-debian-7.7-i386.json

build7qemu:
	/usr/bin/time -v packer build --only=qemu jasonmar-debian-7.7-i386.json

build7vboxdebug:
	/usr/bin/time -v packer build -debug --only=virtualbox-iso jasonmar-debian-7.7-i386.json

build7vbox:
	/usr/bin/time -v packer build --only=virtualbox-iso jasonmar-debian-7.7-i386.json

beep:
	@echo "beep"
	@aplay /usr/share/sounds/alsa/Front_Center.wav
