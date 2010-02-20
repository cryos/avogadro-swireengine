# Example project building an external plugin against installed Avogadro
# library. See http://avogadro.openmolecules.net/ for more information.

# Project name - plugin name or something meaningful
project(SWireEngine)

# Minimum version of CMake that can be used
cmake_minimum_required(VERSION 2.6)

# Find the Avogadro library if it is installed
find_package(Avogadro 0.1.0 REQUIRED)
# Set up the build environment
include(${Avogadro_USE_FILE})
include_directories(${CMAKE_CURRENT_BINARY_DIR})

# Build your plugin using the default options
avogadro_plugin(swireengine swireengine.cpp)

