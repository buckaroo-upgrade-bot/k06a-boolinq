load('//:subdir_glob.bzl', 'subdir_glob')
load('//:buckaroo_macros.bzl', 'buckaroo_deps_from_package')

cxx_library(
  name = 'boolinq',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('include/boolinq', 'boolinq.h'),
  ]),
  visibility = [
    'PUBLIC',
  ],
)

cxx_test(
  name = 'test',
  deps = [
    ':boolinq',
    'buckaroo.github.buckaroo-pm.google-googletest//:googlemock',
    'buckaroo.github.buckaroo-pm.google-googletest//:googletest',
  ],
  srcs = glob(['test/*.cpp'], exclude=['test/ToContainerTest.cpp'])
)
