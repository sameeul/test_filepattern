cmake_minimum_required(VERSION 3.2)
project(TestFilepattern)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(test_fp main.cpp)

find_package(filepattern REQUIRED)
target_link_libraries(test_fp PRIVATE filepattern::filepattern)