TOPDIR?=../../../..
include $(TOPDIR)/build-support/globals.mk

SUBDIRS=
PROGS=
OBJS += lv_font_dejavu_10.o
OBJS += lv_font_dejavu_20.o
OBJS += lv_font_dejavu_30.o
OBJS += lv_font_dejavu_40.o
OBJS += lv_font_dejavu_10_cyrillic.o
OBJS += lv_font_dejavu_20_cyrillic.o
OBJS += lv_font_dejavu_30_cyrillic.o
OBJS += lv_font_dejavu_40_cyrillic.o
OBJS += lv_font_dejavu_10_latin_sup.o
OBJS += lv_font_dejavu_20_latin_sup.o
OBJS += lv_font_dejavu_30_latin_sup.o
OBJS += lv_font_dejavu_40_latin_sup.o
OBJS += lv_font_symbol_10.o
OBJS += lv_font_symbol_20.o
OBJS += lv_font_symbol_30.o
OBJS += lv_font_symbol_40.o
INSTDIR=$(INSTALLROOT)/include/lvgl/lv_misc/lv_fonts

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
