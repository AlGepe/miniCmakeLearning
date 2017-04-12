cmake_minimum_required(VERSION 2.8)

set(CMAKE_VERBOSE_MAKEFILE 1)
#Set CMake behaviour
#CMAKE_POLICY(set CMP0004 OLD)

# Files to compile and name of executable
set(EXECUTABLE_OUTPUT_PATH "${CMAKE_BINARY_DIR}/bin")

# Compiler flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")

#include directories
include_directories(SYSTEM)

#set(SRC main.cpp)

include_directories("${CMAKE_CURRENT_SOURCE_DIR}")
add_executable(Test main.cpp)
