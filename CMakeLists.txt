cmake_minimum_required(VERSION 3.13)
project(cpp)

set(CMAKE_CXX_STANDARD 98)

include_directories(code)

# add_definitions(-DALLOW_INTERSECTION)
# add_definitions(-DCLAMP)
# add_definitions(-DSOG_RELATIVE)
# add_definitions(-DTESS_UNIFORM)
# add_definitions(-DTESS_NONE)
# add_definitions(-DEDGE_TEST_CONVEXITY)
# add_definitions(-DEDGE_TEST_FLIPDIAGONAL)
# add_definitions(-DEDGE_TEST_NEW)

add_executable(dc
        code/dc.cpp
        code/eigen.cpp
        code/octree.cpp)

# See: https://stackoverflow.com/questions/5805874/the-proper-way-of-forcing-a-32-bit-compile-using-cmake
set_target_properties(dc PROPERTIES COMPILE_FLAGS "-m32" LINK_FLAGS "-m32")
