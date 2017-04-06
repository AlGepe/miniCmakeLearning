cmake_minimum_required (VERSION 2.6)
project (Test)
# The version number.
set (Test_VERSION_MAJOR 0)
set (Test_VERSION_MINOR 1)
 
# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
	  "${PROJECT_SOURCE_DIR}/TestConfig.h.in"
		  "${PROJECT_BINARY_DIR}/TestConfig.h"
			  )
			 
			# add the binary tree to the search path for include files
			# so that we will find TestConfig.h
			include_directories("${PROJECT_BINARY_DIR}")
			 
			# add the executable
			add_executable(Test main.cpp)
