# swfpack - configure.ac
# Copyright (c) 2016 Arkadiusz Bokowy

AC_INIT([swfpack], [1.0.0], [arkadiusz.bokowy@gmail.com])
AM_INIT_AUTOMAKE([foreign -Wall -Werror])

AC_CONFIG_HEADERS([config.h])

AC_PROG_CC
AC_PROG_INSTALL
AM_PROG_CC_C_O

# support for debugging
AC_ARG_ENABLE([debug],
	AS_HELP_STRING([--enable-debug], [enable debugging support]))
AM_CONDITIONAL([ENABLE_DEBUG], [test "x$enable_debug" = "xyes"])
AM_COND_IF([ENABLE_DEBUG], [
	AC_DEFINE([DEBUG], [1], [Define to 1 if the debugging is enabled])
])

PKG_CHECK_MODULES([LZMA], [liblzma])
PKG_CHECK_MODULES([ZLIB], [zlib])

AC_CONFIG_FILES([Makefile src/Makefile test/Makefile])
AC_OUTPUT
