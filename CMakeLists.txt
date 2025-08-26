cmake_minimum_required(VERSION 3.16)

project(curlite LANGUAGES CXX)

# Generate compile_commands.json
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(CURL REQUIRED)

add_library(curlite SHARED curlite.cpp)

target_link_libraries(curlite CURL::libcurl)
