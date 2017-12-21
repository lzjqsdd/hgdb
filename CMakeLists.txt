cmake_minimum_required (VERSION 3.0)
project (hgdb)

add_definitions(-std=c++11)
set(CMAKE_BUILD_TYPE Debug)

set(INCLUDE_DIR "./include")
set(LIB_DIR "./lib")

include_directories(
)

link_directories(
)

set(CMAKE_C_FLAGS_DEBUG "-g -Wall -o0")
set(CMAKe_C_FLAGS_RELEASE "-g -Wall -02")

set(SRC_LIST
    src/main.cpp
)

add_subdirectory(./test)

add_executable(hgdb
    ${SRC_LIST}
)

target_link_libraries(hgdb
    ncurses
)
