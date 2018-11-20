#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.
AC_PREREQ([2.69])
AC_INIT([opx-base-model], [3.166.0], [ops-dev@lists.openswitch.net])
AM_INIT_AUTOMAKE([foreign subdir-objects])
AC_CONFIG_SRCDIR([yang-models])
AC_CONFIG_HEADERS([config.h])
LT_INIT([shared])
AM_MAINTAINER_MODE([enable])

# Checks for programs.
AC_PROG_CXX
AC_PROG_AWK
AC_PROG_CC
AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AC_PROG_RANLIB
#AM_PATH_PYTHON

# Checks for libraries.
#AC_CHECK_LIB([pthread], [pthread_self])
#AC_CHECK_LIB([rt], [main])

# Python is needed for the C++ bindings.
#AM_PATH_PYTHON([2.7])

# Checks for header files.
AC_CHECK_HEADERS([inttypes.h limits.h stddef.h stdint.h stdlib.h string.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_INT64_T
AC_TYPE_SIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([memmove memset strstr strtoul])

AC_SUBST(YANG_OUTPUT, $srcdir/opx)
AC_CONFIG_COMMANDS([mkdir], [$MKDIR_P opx])

#AC_CHECK_PROG([python_pip], [pip], [yes], [no])
#AM_CONDITIONAL([FOUND_PIP], [test "x$python_pip" = xyes])
#AM_COND_IF([FOUND_PIP], , [AC_MSG_ERROR([required program 'pip' not found])])

#AC_CHECK_PROG([pyang], [pyang], [yes], [no])
#AM_CONDITIONAL([FOUND_PYANG], [test "x$pyang" = xyes])
#AM_COND_IF([FOUND_PYANG], , [AC_CONFIG_COMMANDS([inst_pyang], [pip install pyang])])

AC_CONFIG_FILES([Makefile])

AC_OUTPUT
