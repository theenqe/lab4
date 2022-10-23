cmake_minimum_required(VERSION 3.16)
 
set(CMAKE_CXX_STANDARD 20)
 
project(solver)
 
add_library(${PROJECT_NAME}_lib STATIC ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib/solver.cpp)
target_include_directories(${PROJECT_NAME}_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib/solver.cpp)
 
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib formatter_ex)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib)
 
add_executable(solver equation.cpp)
 
target_link_libraries(${PROJECT_NAME} formatter_ex solver_lib)
