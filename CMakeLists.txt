cmake_minimum_required(VERSION 2.8)

project (xxhash)

set(SRC
./xxhash.c
)

include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}
)

add_library(xxhash STATIC
  ${SRC}
)

INSTALL(
  TARGETS xxhash
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
  COMPONENT library
)

INSTALL(FILES xxhash.h
        DESTINATION "include"
)
