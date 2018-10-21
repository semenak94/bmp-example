cmake_minimum_required(VERSION 2.8)

set(project "bmp-example")
project(${project})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")

find_package(boost REQUIRED multiprecision)
if(Boost_FOUND)
  include_directories (SYSTEM ${Boost_INCLUDE_DIR})
endif()

file(GLOB SOURCES "src/*.cpp")
add_executable (${project} ${SOURCES})
