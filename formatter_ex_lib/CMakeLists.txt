cmake_minimum_required(VERSION 3.10)
 
set(CMAKE_CXX_STANDARD 20)
 
project(formatter_ex)
 
add_library(${PROJECT_NAME} STATIC formatter_ex.cpp)
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
 
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib formatter_lib)
 
target_link_libraries(${PROJECT_NAME} formatter)
