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

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADERS([libintl.h limits.h stdlib.h string.h strings.h sys/param.h sys/time.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_TYPE_PID_T
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_ERROR_AT_LINE
AC_FUNC_FORK
AC_FUNC_MALLOC
AC_FUNC_WAIT3
AC_CHECK_FUNCS([getpagesize gettimeofday memset strerror])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
