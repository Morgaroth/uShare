ifeq (,$(wildcard ../config.mak))
$(error "config.mak is not present, run configure !")
endif
include ../config.mak

CONF_FILE  = "ushare.conf"
INITD_FILE = "ushare"

EXTRADIST = $(CONF_FILE) $(INITD_FILE)

all:

clean:

distclean:

install:
	$(INSTALL) -d $(DESTDIR)$(sysconfdir)
	$(INSTALL) -m 644 $(CONF_FILE) $(DESTDIR)$(sysconfdir)
	$(INSTALL) -d $(DESTDIR)$(sysconfdir)/init.d
	$(INSTALL) -m 755 $(INITD_FILE) $(DESTDIR)$(sysconfdir)/init.d

dist-all:
	cp $(EXTRADIST) $(SRCS) Makefile $(DIST)

.PHONY: clean disctlean install dist-all
