#Begin--Makefile
KERNELVERSION:=`uname -r`
KERNELDIR:=/lib/modules/$(KERNELVERSION)/build
PWD:=$(shell pwd)
INSTALLDIR:=/home/yunwang/workspace/ko

obj-m:=hello.o

modules:
	@echo "Building hello module..."
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules

install: modules
	cp hello.ko $(INSTALLDIR)

clean:
	@rm -rf *.o *.ko *.mod.c *.mod.o *.order *.symvers .*.ko.cmd .*.mod.o.cmd .*.o.cmd .tmp_versions
.PHONY: modules install clean

#End--Makefile
