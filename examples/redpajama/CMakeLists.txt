#
# redpajama

set(TEST_TARGET redpajama)
add_executable(${TEST_TARGET} main.cpp)
target_link_libraries(${TEST_TARGET} PRIVATE ggml common common-ggml)

if (MSVC)
    target_compile_features(${TEST_TARGET} PUBLIC cxx_std_20)
endif()

#
# redpajama-quantize

set(TEST_TARGET redpajama-quantize)
add_executable(${TEST_TARGET} quantize.cpp)
target_link_libraries(${TEST_TARGET} PRIVATE ggml common common-ggml)

if (MSVC)
    target_compile_features(${TEST_TARGET} PUBLIC cxx_std_20)
endif()
