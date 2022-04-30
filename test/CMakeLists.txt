cmake_minimum_required(VERSION 3.16)

set(TEST_BIN ${PROJECT_NAME}-test)
project(${TEST_BIN})
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/libs/googletest)

file(GLOB SRC_TEST ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)
add_executable(${TEST_BIN} ${SRC_TEST})
target_link_libraries(${TEST_BIN} PRIVATE GTest::gmock GTest::gtest GTest::gmock_main GTest::gtest_main)