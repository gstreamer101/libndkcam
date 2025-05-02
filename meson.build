project(
  'libndkcam',
  'c',
  version: '0.1.0',
  license: 'Apache-2.0',
  meson_version: '>= 0.56'
)

ndkcam_version = meson.project_version()
ndkcam_soversion = '0'

glib_dep = dependency('glib-2.0', version: '>= 2.56')
gobject_dep = dependency('gobject-2.0', version: '>= 2.56')

# Get ANDROID_NDK environment variable
android_ndk_path = get_option('android_ndk_path')
if android_ndk_path == ''
  error('Please provide the -Dandroid_ndk_path option or set it in meson_options.txt.')
endif

android_ndk_inc_path = join_paths(android_ndk_path, 'sources', 'camera', 'ndk')
android_ndk_cpp_args = ['-I' + android_ndk_inc_path]

message('Using Android NDK include path: ' + join_paths(android_ndk_path, 'sources', 'camera', 'ndk'))

# Include + subdir
#subdir('ndkcam')
#subdir('libndkcam')
#subdir('tests')
#subdir('examples')

pkg_mod = import('pkgconfig')

pkg_mod.generate(
  name: 'libndkcam',
  description: 'GObject-based wrapper for Android Camera NDK (Camera2 NDK)',
  version: ndkcam_version,
  libraries: ndkcam_lib,
  requires: ['glib-2.0', 'gobject-2.0'],
  subdirs: ['ndkcam'],
  install_dir: join_paths(get_option('libdir'), 'pkgconfig')
)

