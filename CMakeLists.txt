cmake_minimum_required(VERSION 3.10)
project(WordleCLI)

set(CXX_STANDARD 17)
set(INCLUDE "include")
set(CURL_LIBRARY "../lib/libcurl")

include_directories(${INCLUDE})

add_definitions(-DCURL_STATICLIB)

add_executable(WordleCLI src/main.cpp)

target_link_libraries(WordleCLI ${CURL_LIBRARY})