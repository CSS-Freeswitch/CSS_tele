include $(top_srcdir)/build/modmake.rulesam
MODNAME=mod_format_cdr

mod_LTLIBRARIES = mod_format_cdr.la
mod_format_cdr_la_SOURCES  = mod_format_cdr.c
mod_format_cdr_la_CFLAGS   = $(AM_CFLAGS)
mod_format_cdr_la_CPPFLAGS = $(CURL_CFLAGS) $(AM_CPPFLAGS)
mod_format_cdr_la_LIBADD   = $(switch_builddir)/libfreeswitch.la
mod_format_cdr_la_LDFLAGS  = $(CURL_LIBS) -avoid-version -module -no-undefined -shared
