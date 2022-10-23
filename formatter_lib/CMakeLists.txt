cmake_minimum_required(VERSION 3.16)
 
set(CMAKE_CXX_STANDARD 20)
 
project(formatter)
 
add_library(${PROJECT_NAME} STATIC formatter.cpp)
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
