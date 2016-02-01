cmake_minimum_required (VERSION 2.6)
project (WalkingCode)

# Set outputing executable files to bin directory
set (CMAKE_RUNTIME_OUTPUT_DIRECTORY "${WalkingCode_SOURCE_DIR}/bin")

# Import custom modules from cmake directory
set (CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${WalkingCode_SOURCE_DIR}/cmake")

# Find paths to required libraries
find_package (SDL2 REQUIRED)

# Add paths to include directories
include_directories(${SDL2_INCLUDE_DIR})

# Add all the source files to SRC_FILES variable recursively
add_subdirectory (src)

# Add executable build
add_executable (WalkingCode ${SRC_FILES})

# Specify libraries to link with
target_link_libraries (WalkingCode ${SDL2_LIBRARY})
