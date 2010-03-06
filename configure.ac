AC_INIT([notification-daemon-engine-nodoka],[0.1.0],
        [https://nodoka.fedorahosted.org/])
AC_CONFIG_SRCDIR([src/nodoka-theme.c])

ENGINE_MAJOR_VERSION=0
ENGINE_MINOR_VERSION=1
ENGINE_MICRO_VERSION=0
ENGINE_DEVEL_VERSION=0

ENGINE_VERSION=$ENGINE_MAJOR_VERSION.$ENGINE_MINOR_VERSION.$ENGINE_MICRO_VERSION

if test "x$ENGINE_DEVEL_VERSION" != "x0"; then
	ENGINE_VERSION=$ENGINE_VERSION.$ENGINE_DEVEL_VERSION
fi

AC_DEFINE_UNQUOTED(ENGINE_MAJOR_VERSION, $ENGINE_MAJOR_VERSION,
	[notification-daemon-engine-nodoka major version.])
AC_DEFINE_UNQUOTED(ENGINE_MINOR_VERSION, $ENGINE_MINOR_VERSION,
	[notification-daemon-engine-nodoka minor version.])
AC_DEFINE_UNQUOTED(ENGINE_MICRO_VERSION, $ENGINE_MICRO_VERSION,
	[notification-daemon-engine-nodoka micro version.])
AC_DEFINE_UNQUOTED(ENGINE_VERSION, "$ENGINE_VERSION",
	[notification-daemon-engine-nodoka version.])


AM_INIT_AUTOMAKE([-Wall -Werror])
AM_MAINTAINER_MODE

AC_DISABLE_STATIC
AC_PROG_LIBTOOL

AC_PROG_CC
AC_PROG_CC_STDC
AC_PROG_INSTALL
AC_PROG_MAKE_SET

PKG_CHECK_MODULES(GTK, gtk+-2.0 >= 2.17.1,, 
                   AC_MSG_ERROR([GTK+-2.18 is required to compile nodoka]))

AC_SUBST(GTK_CFLAGS)
AC_SUBST(GTK_LIBS)

AC_CONFIG_HEADERS([src/config.h])
AC_CONFIG_FILES([Makefile src/Makefile])

AC_OUTPUT

echo "Now run make."
