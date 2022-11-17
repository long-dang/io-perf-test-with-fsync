include(CMakePrintHelpers)
cmake_minimum_required(VERSION 3.24)

project(io-perf-test)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

set(BUILD_SHARED_LIBS OFF)
set(CMAKE_EXE_LINKER_FLAGS "-static -static-libgcc")

include_directories(src/main)
file(GLOB_RECURSE main_sources src/main/*.c)

add_executable(io-perf-test ${main_sources})
