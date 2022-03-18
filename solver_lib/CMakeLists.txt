cmake_minimum_required(VERSION 3.4)
project(solver)
add_library(solver STATIC ${CMAKE_CURRENT_SOURCE_DIR}/solver.cpp)
target_include_directories(solver PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
