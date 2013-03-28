#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.63])
AC_INIT([deviceQuery], [1.0], [wqren@live.cn])
AM_INIT_AUTOMAKE([deviceQuery], [1.0])
AC_CONFIG_SRCDIR([deviceQuery.cpp])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_FILES([Makefile])
# Checks for programs.
AC_PROG_CXX

# Checks for libraries.
#CUDA_PATH="/usr/local/cuda"
#AC_SUBST([CUDA_PATH], ["/usr/local/cuda-5.0"])
AC_ARG_WITH([cuda-path],
	    [AS_HELP_STRING([--with-cuda-path], [location of cuda sdk])],
            [CUDA_PATH="$withval"],
            [CUDA_PATH="/usr/local/cuda"])
AC_SUBST([CUDA_PATH])
AC_SUBST([CUDA_CFLAGS], ["-I${CUDA_PATH}/include -I${CUDA_PATH}/samples/common/inc"])
AC_SUBST([CUDA_LDFLAGS], ["-L${CUDA_PATH}/lib64 -lcudart"])


# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE

# Checks for library functions.

AC_OUTPUT
