cmake_minimum_required(VERSION 2.8)
set(CMAKE_TRY_COMPILE_TARGET_TYPE "STATIC_LIBRARY")
project(ann)
IF(APPLE)
    # Fix linking on 10.14+. See https://stackoverflow.com/questions/54068035
    LINK_DIRECTORIES(/usr/local/lib)
ENDIF()

add_definitions(-DDLL_EXPORTS)
include_directories(${PROJECT_SOURCE_DIR}/include/)

add_subdirectory(src)
add_subdirectory(test)
add_subdirectory(sample)
add_subdirectory(ann2fig)

install(DIRECTORY ${PROJECT_SOURCE_DIR}/include/ TYPE INCLUDE)
