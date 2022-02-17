cmake_minimum_required(VERSION 3.16.0 FATAL_ERROR)

project(sbf_cpp
    VERSION 0.1
    LANGUAGES CXX
)

if(PROJECT_SOURCE_DIR STREQUAL PROJECT_BINARY_DIR)
    message(
        FATAL_ERROR
        "In-source builds are not supported. Please make a new directory (i.e. build directory) and run cmake from there."
    )
endif()


add_library(sbf_cpp INTERFACE)
target_include_directories(sbf_cpp INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include")

if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
    include(CTest)
    add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/tests")
endif()
