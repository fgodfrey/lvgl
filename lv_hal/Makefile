TOPDIR?=../../..
include $(TOPDIR)/build-support/globals.mk

SUBDIRS=
PROGS=
OBJS += lv_hal_disp.o
OBJS += lv_hal_indev.o
OBJS += lv_hal_tick.o
INSTDIR=$(INSTALLROOT)/include/lvgl/lv_hal

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
