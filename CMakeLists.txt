cmake_minimum_required(VERSION 2.8.9)
project (utils)

set(utils_VERSION_MAJOR 0)
set(utils_VERSION_MINOR 1)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_C_FLAGS "-Wall")

include_directories(include)

add_library(utils SHARED src/utils.c include/utils.h)

install(TARGETS utils DESTINATION lib)
install(FILES include/utils.h DESTINATION include/libutils)
