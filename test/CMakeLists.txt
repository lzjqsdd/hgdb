cmake_minimum_required (VERSION 3.0)
project (hgdbtest)

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
    tutorial.cpp
)


add_executable(hgdb_test
    ${SRC_LIST}
)

target_link_libraries(hgdb_test
    ncurses
)
