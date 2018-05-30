TOPDIR?=../../..
include $(TOPDIR)/build-support/globals.mk

SUBDIRS=
PROGS=
OBJS += lv_group.o
OBJS += lv_indev.o
OBJS += lv_obj.o
OBJS += lv_refr.o
OBJS += lv_style.o
OBJS += lv_vdb.o
INSTDIR=$(INSTALLROOT)/include/lvgl/lv_core

all: headers build install

build: $(OBJS)

install:
	install -m 755 -d $(INSTALLROOT)/lib
	install -m 555 libvgl.a $(INSTALLROOT)/lib

headers:
	$(INSTALL) -d -m 755 $(INSTDIR)
	for file in *.h ; do 				\
		$(INSTALL) -m 444 $$file $(INSTDIR) ;	\
	done

clean:
	rm -f $(PROGS) *.o

include $(TOPDIR)/build-support/base-rules.mk
