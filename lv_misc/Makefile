TOPDIR?=../../..
include $(TOPDIR)/build-support/globals.mk

SUBDIRS=lv_fonts
PROGS=
OBJS += lv_font.o
OBJS += lv_circ.o
OBJS += lv_area.o
OBJS += lv_task.o
OBJS += lv_fs.o
OBJS += lv_anim.o
OBJS += lv_mem.o
OBJS += lv_ll.o
OBJS += lv_color.o
OBJS += lv_txt.o
OBJS += lv_ufs.o
OBJS += lv_trigo.o
OBJS += lv_math.o
INSTDIR=$(INSTALLROOT)/include/lvgl/lv_misc

all: headers build install

build: $(OBJS)
	for DIR in $(SUBDIRS) ; do 			\
		$(MAKE) -C $$DIR build TOPDIR=$(TOPDIR)/.. ;		\
	done


install: ;

headers:
	$(INSTALL) -d -m 755 $(INSTDIR)
	for DIR in $(SUBDIRS) ; do	 			\
		$(MAKE) -C $$DIR headers TOPDIR=$(TOPDIR)/.. ;	\
	done

	for file in *.h ; do 				\
		$(INSTALL) -m 444 $$file $(INSTDIR) ;	\
	done

clean:
	for DIR in $(SUBDIRS) ; do	 			\
		$(MAKE) -C $$DIR clean TOPDIR=$(TOPDIR)/.. ;	\
	done
	rm -f $(PROGS) *.o

include $(TOPDIR)/build-support/base-rules.mk
