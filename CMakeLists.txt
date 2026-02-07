cmake_minimum_required(VERSION 4.2)

project(Simpleton-Engine LANGUAGES CXX)

set(target ${PROJECT_NAME})
add_library(${target} INTERFACE)
target_include_directories(${target} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})

if(PROJECT_IS_TOP_LEVEL)
add_subdirectory(Pack)
add_subdirectory(Test)
endif(PROJECT_IS_TOP_LEVEL)