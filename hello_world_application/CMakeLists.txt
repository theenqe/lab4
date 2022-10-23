cmake_minimum_required(VERSION 3.16)
 
set(CMAKE_CXX_STANDARD 20)
 
project(hello_world)
 
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib formatter_ex)
 
add_executable(${PROJECT_NAME} hello_world.cpp)
 
target_link_libraries(${PROJECT_NAME} formatter_ex)
