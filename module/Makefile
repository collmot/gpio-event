#############################################################################
#
#	Makefile for building the gpio-event kernel module
#
#############################################################################

ifneq ($(KERNELRELEASE),)
# call from kernel build system

obj-m	:= gpio-event-drv.o

else
# normal makefile - just goes to kbuild

KDIR ?= /lib/modules/`uname -r`/build

default:
	$(MAKE) -C $(KDIR) M=$$PWD

clean:
	$(MAKE) -C $(KDIR) M=$$PWD clean

help:
	$(MAKE) -C $(KDIR) M=$$PWD help

modules:
	$(MAKE) -C $(KDIR) M=$$PWD modules

modules_install:
	$(MAKE) -C $(KDIR) M=$$PWD modules_install
endif

