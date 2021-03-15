## Process this file with automake to produce Makefile.in
## Created by Anjuta

## Process this file with automake to produce Makefile.in
## Created by Anjuta

SUBDIRS = po

dist_doc_DATA = \
        README \
        COPYING \
        AUTHORS \
        ChangeLog \
        INSTALL \
        NEWS


INTLTOOL_FILES = intltool-extract.in \
        intltool-merge.in \
        intltool-update.in

AM_CPPFLAGS = \
        -DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
        -DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
        -DPACKAGE_DATA_DIR=\""$(pkgdatadir)"\" \
        -IProStack-updates/src \
        $(PROSTACK-UPDATES_CFLAGS)

AM_CFLAGS =\
         -Wall\
         -g

bin_PROGRAMS = pckupd

pckupd_SOURCES = \
        ProStack-updates/src/main.cpp

pckupd_HEADERS = 

pckupddir = \
        $(includedir)/pckupd

pckupd_CXXFLAGS = -fPIC \
                -fopenmp

pckupd_CFLAGS = -fPIC

pckupd_LDFLAGS = -fPIC

pckupd_LDADD = $(PROSTACK-UPDATES_LIBS)

if NATIVE_WIN32
pckupd_LDFLAGS += -mwindows
endif

EXTRA_DIST = \
        $(INTLTOOL_FILES)

DISTCLEANFILES = intltool-extract \
        intltool-merge \
        intltool-update \
        po/.intltool-merge-cache


# Remove doc directory on uninstall
uninstall-local:
        -rm -r $(docdir)
