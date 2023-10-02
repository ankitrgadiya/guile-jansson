AC_INIT([guile-jansson], [0.1])
AC_CONFIG_SRCDIR([jansson.scm.in])
AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([-Wall -Werror foreign])

GUILE_PKG([3.0])
GUILE_PROGS
if test "x$GUILD" = "x"; then
   AC_MSG_ERROR(['guild' binary not found; please check your guile-3.x installation.])
fi

PKG_CHECK_MODULES([JANSSEN], [jansson])
JANSSON_LIBDIR="`"$PKG_CONFIG" jansson --variable libdir`"
AC_SUBST([JANSSON_LIBDIR])


AC_CONFIG_FILES([Makefile jansson.scm])
AC_CONFIG_FILES([pre-inst-env], [chmod +x pre-inst-env])

AC_OUTPUT
