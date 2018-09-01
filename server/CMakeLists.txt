cmake_minimum_required(VERSION 3.5)

find_package(Boost 1.58 REQUIRED COMPONENTS system)
include_directories(client ${Boost_INCLUDE_DIRS})
add_executable(client main.cpp)
link_directories(client ${Boost_LIBRARY_DIRS})
target_link_libraries(client LINK_PUBLIC ${Boost_LIBRARIES})
