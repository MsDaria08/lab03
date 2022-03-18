cmake_minimum_required(VERSION 3.4)
project(hello_world)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib
		 ${CMAKE_CURRENT_BINARY_DIR}/formatter_ex)
add_executable(hello_world hello_world.cpp)
target_link_libraries(hello_world formatter_ex)
