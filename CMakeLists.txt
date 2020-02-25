PROJECT(test_package)
cmake_minimum_required(VERSION 3.1.2)

set(CMAKE_VERBOSE_MAKEFILE TRUE)

include(conanbuildinfo.cmake)
CONAN_BASIC_SETUP()

ADD_EXECUTABLE(mytest test_package.cpp)
TARGET_LINK_LIBRARIES(mytest ${CONAN_LIBS})
