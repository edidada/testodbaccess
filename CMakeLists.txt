cmake_minimum_required(VERSION 3.8)
project(testodbaccess)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -DDATABASE_MYSQL")

add_executable(testodbaccess driver.cxx person-odb.cxx)
add_executable(travis_driver travis_driver.cxx person-odb.cxx)

target_link_libraries(testodbaccess libodb-mysql.so libodb.so)
target_link_libraries(travis_driver libodb-mysql.so libodb.so)
