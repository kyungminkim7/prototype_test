cmake_minimum_required(VERSION 3.20)
project(PrototypeTest)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

enable_testing()
include(GetGoogleTest)
include(GoogleTest)

add_executable(prototype_test prototype_test.cpp)

target_link_libraries(prototype_test
    gtest
    gmock
    gtest_main
)

gtest_discover_tests(prototype_test)