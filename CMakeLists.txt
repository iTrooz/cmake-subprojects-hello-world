cmake_minimum_required(VERSION 3.16)

add_library(lib1 lib1/src/lib1.cpp)
add_library(lib2 lib2/src/lib2.cpp)
target_include_directories(lib1 PUBLIC lib1/include)
target_include_directories(lib2 PUBLIC lib2/include)

add_executable(exe1 exe1.cpp)
target_link_libraries(exe1 lib1 lib2)
