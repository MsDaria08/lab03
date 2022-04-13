cmake_minimum_required(VERSION 3.12)

project(question)

option(CPACK_GENERATOR_RPM OFF)

add_subdirectory(../formatter_ex_lib formatter_ex)
add_subdirectory(../solver_lib solver_lib)
add_executable(question equation.cpp)
target_link_libraries(question formatter_ex solver)

install(TARGETS question RUNTIME DESTINATION bin)
set(CPACK_SOURCE_GENERATOR "TGZ;ZIP")

if(CPACK_GENERATOR_RPM)
    set(CPACK_GENERATOR "RPM")
endif()

include(CPack)

unset(CPack)
unset(CPACK_GENERATOR_RPM CACHE)