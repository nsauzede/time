#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
VERSION=1.7
AC_SUBST(VERSION)
PACKAGE=time
AC_SUBST(PACKAGE)
AC_INIT([time],[1.7])
AC_CONFIG_SRCDIR([error.c])
AC_CONFIG_HEADERS([config.h])

AM_INIT_AUTOMAKE

# Checks for programs.
AC_PROG_CC
AC_PROG_CPP
AC_PROG_INSTALL

# Checks for libraries.

# Checks for header files.
AC_HEADER_STDC
AC_HEADER_SYS_WAIT
AC_CHECK_HEADERS([libintl.h limits.h stdlib.h string.h strings.h sys/param.h sys/time.h unistd.h sys/rusage.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_CHECK_HEADER_STDBOOL
AC_TYPE_PID_T
AC_TYPE_SIZE_T
AC_TYPE_SIGNAL

AC_MSG_CHECKING(for struct timeval in sys/time.h)
AC_EGREP_HEADER(tv_usec, sys/time.h, have_tv=yes, have_tv=no)
AC_MSG_RESULT($have_tv)
test $have_tv = yes && AC_DEFINE([HAVE_TIMEVAL], [], [Define to 1 if you have 'struct timeval' in the <sys/time.h> header file.])

# Checks for library functions.
AC_FUNC_VPRINTF
AC_FUNC_ERROR_AT_LINE
AC_FUNC_FORK
AC_FUNC_MALLOC
AC_FUNC_WAIT3
AC_CHECK_FUNCS([gettimeofday memset strerror])

AC_MSG_CHECKING(for getpagesize)
AC_TRY_LINK([#include <sys/param.h>],
[getpagesize();], have_gp=yes, have_gp=no)
AC_MSG_RESULT($have_gp)
test $have_gp = yes && AC_DEFINE([HAVE_GETPAGESIZE], [], [Define to 1 if you have the `getpagesize' function.])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
