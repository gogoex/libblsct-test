AC_INIT([blsctlib-driver], [1.0])
AC_CONFIG_SRCDIR([src/main.cpp])
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE([foreign])
AC_CONFIG_FILES([Makefile src/Makefile])
AC_CONFIG_MACRO_DIRS([m4])
AC_PROG_CXX
AC_PROG_RANLIB
AC_PROG_LIBTOOL

AC_CANONICAL_HOST

AC_MSG_CHECKING([for Darwin])
case "$host" in
  *darwin*)
    AC_MSG_RESULT([yes])
    am_os_darwin=true
    ;;
  *)
    AC_MSG_RESULT([no])
    am_os_darwin=false
    ;;
esac

AM_CONDITIONAL([OS_DARWIN], [test "$am_os_darwin" = true])

AC_OUTPUT
echo "os_darwin = $am_os_darwin"
