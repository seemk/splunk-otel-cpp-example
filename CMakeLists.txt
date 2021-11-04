cmake_minimum_required(VERSION 3.4)
project(example-trace)
set(CMAKE_CXX_STANDARD 11)

include(${CMAKE_BINARY_DIR}/conan_paths.cmake)

find_package(SplunkOpenTelemetry REQUIRED)

add_executable(example example.cpp)

target_link_libraries(example PRIVATE ${SplunkOpenTelemetry_LIBRARIES})
target_include_directories(example PRIVATE ${SplunkOpenTelemetry_INCLUDE_DIRS})
