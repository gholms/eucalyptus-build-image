AC_INIT([eucalyptus-build-image], [5])

INSTALL_TREE=http://linux.mirrors.es.net/centos/7/os/x86_64/
BASE_MIRROR=${INSTALL_TREE}
UPDATES_MIRROR=http://linux.mirrors.es.net/centos/7/updates/x86_64/
EPEL_MIRROR=http://linux.mirrors.es.net/epel/7/x86_64/

AC_ARG_WITH(install-tree,
    [  --with-install-tree=<dir>       the location of the install tree],
    [INSTALL_TREE="${withval}"])
AC_ARG_WITH(updates-mirror,
    [  --with-updates-mirror=<dir>     the location of the updates mirror],
    [UPDATES_MIRROR="${withval}"])
AC_ARG_WITH(epel-mirror,
    [  --with-epel-mirror=<dir>        the location of the EPEL mirror],
    [EPEL_MIRROR="${withval}"])

AC_PATH_PROG(PYTHON, python)
AC_PATH_PROG(VIRSH, virsh)
AC_PATH_PROG(VIRT_INSTALL, virt-install)
AC_PATH_PROG(VIRT_SYSPREP, virt-sysprep)
AC_PATH_PROG(VIRT_SPARSIFY, virt-sparsify)

AC_CONFIG_FILES([
    Makefile
    centos-7-builder.ks
    centos-7-builder.yml
])
AC_SUBST(INSTALL_TREE)
AC_SUBST(BASE_MIRROR)
AC_SUBST(UPDATES_MIRROR)
AC_SUBST(EPEL_MIRROR)
AC_SUBST(VIRSH)
AC_SUBST(VIRT_INSTALL)
AC_SUBST(VIRT_SYSPREP)
AC_SUBST(VIRT_SPARSIFY)
AC_OUTPUT
