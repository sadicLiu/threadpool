cmake_minimum_required(VERSION 3.16)
project(threadpool)

enable_language(C)
enable_language(CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "-pthread ${CMAKE_CXX_FLAGS}")  #force pthread to avoid bugs in some cmake setups
set(CMAKE_C_FLAGS "-pthread ${CMAKE_C_FLAGS}")

add_executable(run main.cpp)