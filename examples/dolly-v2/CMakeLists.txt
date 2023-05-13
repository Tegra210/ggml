#
# dollyv2

set(TEST_TARGET dollyv2)
add_executable(${TEST_TARGET} main.cpp)
target_link_libraries(${TEST_TARGET} PRIVATE ggml common common-ggml)

if (MSVC)
    target_compile_features(common PUBLIC cxx_std_20)
    target_compile_features(common-ggml PUBLIC cxx_std_20)
endif()

#
# dollyv2-quantize

set(TEST_TARGET dollyv2-quantize)
add_executable(${TEST_TARGET} quantize.cpp)
target_link_libraries(${TEST_TARGET} PRIVATE ggml common common-ggml)

if (MSVC)
    target_compile_features(common PUBLIC cxx_std_20)
    target_compile_features(common-ggml PUBLIC cxx_std_20)
endif()

