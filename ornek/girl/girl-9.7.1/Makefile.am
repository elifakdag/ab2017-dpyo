SUBDIRS = data help man src po

datadir = @datadir@

EXTRA_DIST = config.rpath m4/ChangeLog  \
	AUTHORS \
	ChangeLog \
	BROADCAST \
	DEBIAN \
	GNOME3 \
	HACKING \
	LETTER \
	MAILINGLIST \
	Makefile \
	NEWS \
	README \
	THANKS \
	TODO \
	VERSION \
	YP-DIRS \
	girl.spec.in

DISTCLEANFILES =                \
        intltool-extract        \
        intltool-merge          \
        intltool-update

MAINTAINERCLEANFILES = \
	$(srcdir)/aclocal.m4 \
	$(srcdir)/config.guess \
	$(srcdir)/config.h.in \
	$(srcdir)/config.sub \
	$(srcdir)/depcomp \
	$(srcdir)/gtk-doc.make \
	$(srcdir)/install-sh \
	$(srcdir)/ltmain.sh \
	$(srcdir)/missing \
	$(srcdir)/mkinstalldirs

-include $(top_srcdir)/git.mk

ACLOCAL_AMFLAGS = -I m4

# Build ChangeLog from GIT history
ChangeLog:
	@if test -f $(top_srcdir)/.git/HEAD; then \
		git log --stat --after="Mon Jul 20 23:47:57 2009" > $@; \
	fi

dist: ChangeLog

.PHONY: ChangeLog
