cmake_minimum_required(VERSION 3.12)
project(malloc_count)

add_library(malloc_count STATIC src/malloc_count.c)
add_library(malloc_count::malloc_count ALIAS malloc_count)

target_include_directories(malloc_count PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)
