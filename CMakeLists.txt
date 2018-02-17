cmake_minimum_required(VERSION 3.9)
project(Boost_Commandline)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

find_package(Boost 1.66.0 COMPONENTS program_options REQUIRED)
include_directories( ${Boost_INCLUDE_DIR} )

add_executable(Boost_Commandline main.cpp)
target_link_libraries(Boost_Commandline LINK_PUBLIC ${Boost_LIBRARIES} )