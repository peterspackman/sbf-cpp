cmake_minimum_required(VERSION 3.16.0 FATAL_ERROR)

project(sbf_cpp
    VERSION 0.1
    LANGUAGES CXX
)


add_library(sbf_cpp INTERFACE)
target_include_directories(sbf_cpp INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include")
