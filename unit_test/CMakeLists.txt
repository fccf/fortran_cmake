cmake_minimum_required(VERSION 2.10)
project(x Fortran)

#static library
file(GLOB src ${CMAKE_CURRENT_SOURCE_DIR}/src/*.f90)
add_library(hello STATIC ${src})

#unit test
enable_testing()
add_subdirectory(src/test)
