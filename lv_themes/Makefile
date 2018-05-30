TOPDIR?=../../..
include $(TOPDIR)/build-support/globals.mk

SUBDIRS=
PROGS=
OBJS += lv_theme_alien.o
OBJS += lv_theme.o
OBJS += lv_theme_default.o
OBJS += lv_theme_night.o
OBJS += lv_theme_templ.o
OBJS += lv_theme_zen.o
OBJS += lv_theme_material.o
INSTDIR=$(INSTALLROOT)/include/lvgl/lv_themes

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
