ACLOCAL_AMFLAGS = -I m4 -I common/m4

if BUILD_EXAMPLES
SUBDIRS_TESTS = tests
else
SUBDIRS_TESTS =
endif

SUBDIRS = gst-libs gst $(SUBDIRS_TESTS) m4 common docs

DISTCHECK_CONFIGURE_FLAGS=--enable-gtk-doc

# Extra clean files so that maintainer-clean removes *everything*
MAINTAINERCLEANFILES = \
	$(GITIGNORE_MAINTAINERCLEANFILES_TOPLEVEL)	\
	$(GITIGNORE_MAINTAINERCLEANFILES_MAKEFILE_IN)	\
	$(GITIGNORE_MAINTAINERCLEANFILES_M4_LIBTOOL)	\
	$(srcdir)/autoregen.sh $(srcdir)/INSTALL	\
	$(NULL)

EXTRA_DIST = \
	configure.ac autogen.sh \
	gstreamer-vaapi.doap

-include $(top_srcdir)/git.mk
