cmake_minimum_required(VERSION 3.16)

set(PROJECT_NAME fun)

project(${PROJECT_NAME} VERSION 1.0 LANGUAGES CXX)

file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)
add_library(${PROJECT_NAME} ${SRC})
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

add_subdirectory(test)