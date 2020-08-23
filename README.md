## DUNFELL YOCTO Release

### This repository is written to support BBB initramfs testing
Attempt to create one generic Open Source BeagleBone Black armv7 A8 platform reference and testing repository.
The YOCTO BeagleBobe Black YOCTO repo used is described @ the following net pointer:

https://jumpnowtek.com/beaglebone/BeagleBone-Systems-with-Yocto.html

### The bash script, customized for the owner's projects purposes (substitutions for the KAS tool)

https://github.com/ZoranStojsavljevic/bbb-yocto/blob/master/dunfell-setup.sh

	Step [1]: Look into the script and customize it for your own project;
	Step [2]: Make the script dunfell-setup.sh executable (permissions 755), and execute it: ./dunfell-setup.sh ;
	Step [3]: Run bitbake -k core-image-minimal ## or whatever core-image-? you need

### The test initramfs BBB image description
Part of the config-initramfs, outlining important part of defconfig (the booting is done solely from initramfs)!

	CONFIG_BLK_DEV_INITRD=y
	CONFIG_RD_GZIP=y
	CONFIG_RD_BZIP2=y
	CONFIG_RD_LZMA=y
	CONFIG_RD_XZ=y
	CONFIG_RD_LZ4=y
	CONFIG_RD_LZO=y
	CONFIG_BLK_DEV_RAM=y
	CONFIG_BLK_DEV_RAM_COUNT=16
	CONFIG_BLK_DEV_RAM_SIZE=16384

### Referent YOCTO Poky BeagleBone distro is also supported:

git clone https://git.yoctoproject.org/git/poky.git
