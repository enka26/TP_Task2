cmake_minimum_required(VERSION 2.8)

project(BLib)

set(SOURSES lib.cpp)
set(HEADERS lib.h)
add_library(Blib ${SOURSES} ${HEADERS})


