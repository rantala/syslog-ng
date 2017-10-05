project('simple', 'c')
glib = dependency('glib-2.0')
gthread = dependency('gthread-2.0')
libsystemd = dependency('libsystemd')
openssl = dependency('openssl')
libcrypto = dependency('libcrypto')
libm = meson.get_compiler('c').find_library('m')
executable('loggen-journal',
	['loggen.c', '../../lib/crypto.c', '../../lib/compat/openssl_support.c'],
	dependencies : [glib, gthread, libsystemd, openssl, libcrypto, libm],
	include_directories : [ include_directories('../../lib/') ],
)
