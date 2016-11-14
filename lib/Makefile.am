noinst_LTLIBRARIES = libcompat.la
libcompat_la_SOURCES = lib.c
libcompat_la_LIBADD = $(LTLIBOBJS)

if CROSS
noinst_LTLIBRARIES += libcompatbuild.la
libcompatbuild_la_SOURCES = lib.c
libcompatbuild_la_LIBADD = $(LTLIBOBJS)

libcompatbuild_LINK = $(LIBTOOL) --tag=CC --mode=link $(CC_FOR_BUILD) \
         $(CFLAGS_FOR_BUILD) $(LDFLAGS_FOR_BUILD) -o $@

$(libcompatbuild_OBJECTS): CC=$(CC_FOR_BUILD)
$(libcompatbuild_OBJECTS): CFLAGS=$(CFLAGS_FOR_BUILD)
$(libcompatbuild_OBJECTS): CPPFLAGS=$(CPPFLAGS_FOR_BUILD)
endif
