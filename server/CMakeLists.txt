cmake_minimum_required(VERSION 3.10)
project(TCPServer)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

include_directories(include)

set(SOURCES
    source/main.cpp
        source/TCPServer.cpp
        )

        add_executable(TCPServer ${SOURCES})

        if(UNIX AND NOT APPLE)
            target_link_libraries(TCPServer pthread)
            endif()

