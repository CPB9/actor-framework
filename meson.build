project('caf', 'cpp', default_options : ['cpp_std=c++11'], version : '0.15.5')

cc = meson.get_compiler('cpp').get_id()

cflags = []
ldflags = []

if cc == 'clang'
  cflags += ['-ftemplate-depth=512', '-ftemplate-backtrace-limit=0']
elif cc == 'gcc'
  cflags += '-Wno-missing-field-initializers'
endif

shared_deps = [dependency('threads')]

system = target_machine.system()

if system == 'windows' and cc == 'gcc'
  cflags += ['-D_WIN32_WINNT=0x0600', '-DWIN32']
  ldflags += ['ws2_32', '-liphlpapi', '-lpsapi']
elif system == 'cygwin'
  cflags += '-U__STRICT_ANSI__'
endif

if system == 'windows'
  ldflags += ['ws2_32', 'iphlpapi']
endif

subdir('libcaf_core')
