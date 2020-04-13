# @file CMakeLists.txt
# 
# CMake files for Memoes
cmake_minimum_required(VERSION 3.10)

# project info
project(Memoes)

# force release debug since used for demonstration
set(CMAKE_BUILD_TYPE Debug)

# C++17 standard
set(CMAKE_CXX_STANDARD 17)

# Test program is all we have now
add_executable(Memoes_t Memoes_t.cpp Memoes.cpp)

# Run test program
add_custom_target(unittest COMMENT "Test Memoes"
                           COMMAND ./Memoes_t
                           DEPENDS Memoes_t)