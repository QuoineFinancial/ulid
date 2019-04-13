cmake_minimum_required(VERSION 3.13)
project(Ulid VERSION 0.1.0)

add_library(ulid)
target_sources(ulid PRIVATE dummy.cpp)
target_include_directories(ulid INTERFACE
        $<INSTALL_INTERFACE:include>
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>)

#install(TARGETS ulid)
install(FILES ulid.hh ulid_struct.hh ulid_uint128.hh
        DESTINATION include/ulid
        )


