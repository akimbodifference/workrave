# Process this file with automake to produce Makefile.in
#
# Copyright (C) 2001, 2002, 2003, 2004, 2005, 2006, 2007, 2008, 2009, 2011 Rob Caelers & Raymond Penners
#


MAINTAINERCLEANFILES = 	\
		aclocal.m4 config.h.in configure stamp-h.in \
		Makefile.in \
		install-sh missing mkinstalldirs config.cache \
		config.log config.status \
		config.guess config.sub depcomp ltmain.sh \
		build-stamp intltool-update.in intltool-update \
		intltool-merge.in intltool-merge \
		intltool-extract.in intltool-extract workrave.spec \
		compile AUTHORS.txt COPYING.txt \
		NEWS.txt README.txt
DISTCLEANFILES = intltool-extract intltool-merge intltool-update

SUBDIRS =      m4 po common backend frontend 
DIST_SUBDIRS = $(SUBDIRS) build contrib

EXTRA_DIST = 	config.xml README.md autogen.sh

DISTCHECK_CONFIGURE_FLAGS = --enable-localinstall

noinst_PROGRAMS =

if PLATFORM_OS_WIN32
dist_pkgdata_DATA = README.txt NEWS.txt AUTHORS.txt COPYING.txt
endif

ACLOCAL_AMFLAGS = -I m4

unix2dos = perl -e 'while (<>) { s/$$/\r/; print; }'

README.txt: README.md
	$(unix2dos) <$^ >$@

NEWS.txt: NEWS
	$(unix2dos) <$^ >$@

AUTHORS.txt: AUTHORS
	$(unix2dos) <$^ >$@

COPYING.txt: COPYING
	$(unix2dos) <$^ >$@
