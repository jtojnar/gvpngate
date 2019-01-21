project(
  'gvpngate',
  'c',
  version: '0.55',
  license: 'GPL-3.0+',
)

prefix = get_option('prefix')
bindir = join_paths(prefix, get_option('bindir'))
datadir = join_paths(prefix, get_option('datadir'))
localedir = join_paths(prefix, get_option('localedir'))
pkgdatadir = join_paths(datadir, meson.project_name())
docdir = join_paths(datadir, 'doc', meson.project_name())
uidir = join_paths(pkgdatadir, 'ui')

gtk = dependency('gtk+-3.0', version : '>= 3.22.4')
uuid = dependency('uuid')

docs = [
  'README',
  'COPYING',
  'AUTHORS',
  'ChangeLog',
  'INSTALL',
  'NEWS',
  'LICENSE',
]
foreach doc : docs
  install_data(doc, install_dir: docdir)
endforeach

install_data('gvpngate.desktop', install_dir: join_paths(datadir, 'applications'))
install_data('gvpngate.png', install_dir: join_paths(datadir, 'icons'))
install_data('gvpngate.png', install_dir: uidir)

subdir('src')
