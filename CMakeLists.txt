cmake_minimum_required(VERSION 3.8)

project(bax-perf VERSION 0.1 LANGUAGES C)

set(CMAKE_C_STANDARD 90)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS OFF)

add_executable(perf-t "tests/perf_test.c")

target_include_directories(perf-t PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}")
target_compile_definitions(perf-t PRIVATE PERF_STATS_ENABLE)
