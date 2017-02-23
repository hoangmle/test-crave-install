project ( test-crave-install )
cmake_minimum_required(VERSION 2.8)

add_definitions(-std=c++11)

find_package(crave REQUIRED)

message(STATUS "includes: ${crave_INCLUDE_DIR}")
message(STATUS "libs:     ${crave_LIBRARIES}")
message(STATUS "defs:     ${crave_DEFINITIONS}")

include_directories(${crave_INCLUDE_DIR})

add_executable(main main.cpp)
target_link_libraries(main ${crave_LIBRARIES})


