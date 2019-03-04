cmake_minimum_required(VERSION 2.8)

project(tpTask2)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")

set(SRC_LIST "C/main.cpp")
set(HDR_LIST "C/main.h")
execute_process(COMMAND python "${CMAKE_CURRENT_LIST_DIR}/A/preparing.py")

add_subdirectory("${CMAKE_CURRENT_LIST_DIR}/B")

include_directories(${CMAKE_CURRENT_LIST_DIR})

add_executable(tpTask2 ${HDR_LIST} ${SRC_LIST})
