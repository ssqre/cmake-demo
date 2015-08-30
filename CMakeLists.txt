cmake_minimum_required (VERSION 2.6)
project(demo)

# The version number.
set (demo_VERSION_MAJOR 1)
set (demo_VERSION_MINOR 0)

# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  "${PROJECT_SOURCE_DIR}/democonfig.h.in"
  "${PROJECT_BINARY_DIR}/democonfig.h"
  )

# add the binary tree to the search path for include files
# so that we will find democonfig.h
include_directories ("${PROJECT_BINARY_DIR}")

add_subdirectory (lib)
add_subdirectory (app)