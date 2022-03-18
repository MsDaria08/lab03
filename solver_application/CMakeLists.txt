cmake_minimum_required(VERSION 3.4)

project(question)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib ${CMAKE_CURRENT_BINARY_DIR}/formatter_ex)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib ${CMAKE_CURRENT_BINARY_DIR}/solver)
add_executable(question ${CMAKE_CURRENT_SOURCE_DIR}/equation.cpp)
target_link_libraries(question formatter_ex solver)
