cmake_minimum_required(VERSION 2.8)
project(ann)

add_definitions(-DDLL_EXPORTS)
include_directories(${PROJECT_SOURCE_DIR}/include/)

add_subdirectory(src)
add_subdirectory(test)
add_subdirectory(sample)
add_subdirectory(ann2fig)

install(DIRECTORY ${PROJECT_SOURCE_DIR}/include/ TYPE INCLUDE)
