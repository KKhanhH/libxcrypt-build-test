cmake_minimum_required(VERSION 3.10)

# Set the project name
project(MyProject)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(MyExecutable main.cpp)

# Find the libxcrypt library
find_library(LIBXCRYPT_LIBRARY NAMES crypt)

# Link the libxcrypt library
target_link_libraries(MyExecutable ${LIBXCRYPT_LIBRARY})