include $(top_srcdir)/build/modmake.rulesam
MODNAME=mod_amd

mod_LTLIBRARIES = mod_amd.la
mod_amd_la_SOURCES  = mod_amd.c
mod_amd_la_CFLAGS   = $(AM_CFLAGS) $(AM_MOD_amd_CXXFLAGS)
mod_amd_la_LIBADD   = $(switch_builddir)/libfreeswitch.la
mod_amd_la_LDFLAGS  = -avoid-version -module -no-undefined -shared
