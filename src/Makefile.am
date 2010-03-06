AM_CPPFLAGS = $(GTK_CFLAGS) $(LIBSEXY_CFLAGS)

enginedir = $(libdir)/notification-daemon-1.0/engines
engine_LTLIBRARIES = libnodoka.la

libnodoka_la_SOURCES = nodoka-theme.c

libnodoka_la_LDFLAGS = -module -avoid-version
libnodoka_la_LIBADD =  $(GTK_LIBS) $(LIBSEXY_LIBS)
