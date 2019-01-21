executable(
  'gvpngate',
  [
    'gvpngate.c',
    'mainwindow.c',
  ],
  dependencies: [
    gtk,
    uuid,
  ],
  c_args: [
    '-DPACKAGE_LOCALE_DIR="@0@"'.format(localedir),
    '-DPACKAGE_SRC_DIR="@0@"'.format(meson.current_source_dir()),
    '-DPACKAGE_DATA_DIR="@0@"'.format(pkgdatadir),
  ],
  install: true,
)

executable(
  'gvpngate_suid',
  [
    'gvpngate_suid.c',
  ],
  install: true,
  install_mode: 'rwsr-xr-x',
)

install_data(
  'gvpngate.ui',
  install_dir: uidir,
)
