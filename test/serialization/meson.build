# SPDX-License-Identifier: CC0-1.0

subdir('generated_serializer')

serialization_tests = [
    ['control_serialization',     'control_serialization.cpp'],
    ['ipa_data_serializer_test',  'ipa_data_serializer_test.cpp'],
]

foreach t : serialization_tests
    exe = executable(t[0], [t[1], 'serialization_test.cpp'],
                     dependencies : libcamera_private,
                     link_with : test_libraries,
                     include_directories : test_includes_internal)
    test(t[0], exe, suite : 'serialization', is_parallel : false)
endforeach
