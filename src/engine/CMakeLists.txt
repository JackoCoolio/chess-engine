cmake_minimum_required(VERSION 3.9.2)
project(CheddarEngine)

set(HEADERS
    board.h
    move.h
    util.h
    core.h
    gen.h
    fill.h
)

set(SOURCE
    board.cpp
    move.cpp
    gen.cpp
    fill.cpp
)

add_library(engine SHARED STATIC ${SOURCE})

install(TARGETS engine DESTINATION ${CHEDDAR_INSTALL_LIB_DIR})

install(FILES ${HEADERS} DESTINATION ${CHEDDAR_INSTALL_INCLUDE_DIR})
