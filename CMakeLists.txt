PROJECT(MyHello)
cmake_minimum_required(VERSION 3.1.2)

set(CMAKE_VERBOSE_MAKEFILE TRUE)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)

CONAN_BASIC_SETUP()

ADD_EXECUTABLE(test_package test_package.cpp)
TARGET_LINK_LIBRARIES(test_package ${CONAN_LIBS})
