file(GLOB LIB_SOURCES *cpp)
add_library(ann SHARED ${LIB_SOURCES})
target_include_directories(ann PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
install(TARGETS ann DESTINATION lib)
