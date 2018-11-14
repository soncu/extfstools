AC_INIT([extfstools], [0.1], [itsme@xs4all.nl])
AM_INIT_AUTOMAKE([foreign -Wall -Werror subdir-objects])
AC_PROG_CXX
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_FILES([Makefile])
AC_OUTPUT

AC_CONFIG_MACRO_DIR([m4])
AX_BOOST_BASE([1.48],, [AC_MSG_ERROR([extfstools needs Boost, but it was not found in your system])])
