cmake_minimum_required(VERSION 3.26)

project(ectool
        VERSION 0.1.0
        LANGUAGES C CXX
)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# find
include("${PROJECT_SOURCE_DIR}/cmake/FindGTest.cmake")

add_library(ectool STATIC)
#add_library(ectool::ectool ALIAS ectool)
target_include_directories(ectool
        PUBLIC
        "$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>"
        "$<INSTALL_INTERFACE:include>"
)

add_subdirectory(lib)
