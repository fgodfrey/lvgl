TOPDIR?=../../..
include $(TOPDIR)/build-support/globals.mk

SUBDIRS=
PROGS=
OBJS += lv_bar.o
OBJS += lv_cb.o
OBJS += lv_ddlist.o
OBJS += lv_kb.o
OBJS += lv_line.o
OBJS += lv_mbox.o
OBJS += lv_roller.o
OBJS += lv_tabview.o
OBJS += lv_btn.o
OBJS += lv_chart.o
OBJS += lv_gauge.o
OBJS += lv_label.o
OBJS += lv_list.o
OBJS += lv_slider.o
OBJS += lv_ta.o
OBJS += lv_btnm.o
OBJS += lv_cont.o
OBJS += lv_img.o
OBJS += lv_led.o
OBJS += lv_lmeter.o
OBJS += lv_page.o
OBJS += lv_sw.o
OBJS += lv_win.o
INSTDIR=$(INSTALLROOT)/include/lvgl/lv_objx

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
