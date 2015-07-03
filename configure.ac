#
# RandNetGen
#
# Copyright 2014 Pol Colomer de Simon.
#
# All rights reserved. Code under License GPLv3.
#
# RandNetGen is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License.
#
# RandNetGen is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with RandNetGen.  If not, see <http://www.gnu.org/licenses/>.
#

AC_PREREQ([2.68])

AC_INIT([randnetgen], [1.0.0], [<pol-email-here>])

RANDNETGEN_MAJOR_VERSION=0
RANDNETGEN_MID_VERSION=0
RANDNETGEN_MINOR_VERSION=0

AC_DEFINE_UNQUOTED([RANDNETGEN_MAJOR_VERSION],RANDNETGEN_MAJOR_VERSION,
	[randnetgen major version])
AC_DEFINE_UNQUOTED([RANDNETGEN_MID_VERSION],RANDNETGEN_MID_VERSION,
	[randnetgen mid version])
AC_DEFINE_UNQUOTED([RANDNETGEN_MINOR_VERSION],RANDNETGEN_MINOR_VERSION,
	[randnetgen minor version])

LT_INIT

AM_INIT_AUTOMAKE

AC_CONFIG_MACRO_DIR([m4])

AC_CONFIG_SRCDIR([src/randnetgen.c])
AC_CONFIG_HEADERS([src/config.h])

# Checks for programs.
AC_PROG_LIBTOOL
AC_PROG_CXX
AM_PROG_LIBTOOL
AC_PROG_CC_C99

AC_SYS_LARGEFILE

AH_VERBATIM([_GNU_SOURCE],
[/* Enable GNU extensions on systems that have them.  */
#ifndef _GNU_SOURCE
#define _GNU_SOURCE
#endif])

AC_CHECK_FUNCS([memset strdup])


# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE
AC_TYPE_SIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC

# Checks for libraries.
AC_CHECK_LIB([m],[cos])
AC_CHECK_LIB([gslcblas],[cblas_dgemm])
AC_CHECK_LIB([gsl],[gsl_blas_dgemm])


AC_HEADER_ASSERT

AC_SUBST([RANDNETGEN_MAJOR_VERSION])
AC_SUBST([RANDNETGEN_MID_VERSION])
AC_SUBST([RANDNETGEN_MINOR_VERSION])

AC_HEADER_ASSERT

AC_CONFIG_FILES([Makefile
		src/Makefile
		])
AC_OUTPUT
