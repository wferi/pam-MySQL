# install this platform-dependent module by the 'install-exec' rules
pamexecdir = @PAM_MODS_DIR@
pamexec_LTLIBRARIES = pam_mysql.la

pam_mysql_la_SOURCES = pam_mysql.c crypto.c crypto-sha1.c crypto-md5.c
pam_mysql_la_LDFLAGS = -module -avoid-version
pam_mysql_la_CPPFLAGS = $(openssl_CFLAGS)
pam_mysql_la_LIBADD   = $(openssl_LIBS) -lpam

EXTRA_DIST = INSTALL.pam-mysql

AM_DISTCHECK_CONFIGURE_FLAGS = --with-pam-mods-dir=\$${prefix}/lib/security
