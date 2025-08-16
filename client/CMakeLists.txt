cmake_minimum_required(VERSION 3.10)
project(TCPClient)


set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

include_directories(include)


set(SOURCES
    source/main.cpp
    source/TCPClient.cpp
)

add_executable(TCPClient ${SOURCES})


if(UNIX AND NOT APPLE)
    target_link_libraries(TCPClient pthread)
endif()
