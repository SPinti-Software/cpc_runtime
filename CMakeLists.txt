cmake_minimum_required (VERSION 3.13)

if (${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR})
	message(FATAL_ERROR "Prevented in-tree build. Please create a build directory outside of the source code and call cmake from there")
endif ()

project (cpc_runtime)

enable_language (C)

set (CMAKE_C_STANDARD 90)
set (CMAKE_C_STANDARD_REQUIRED ON)
set (CMAKE_C_EXTENSIONS OFF)

set (CMAKE_C_FLAGS_RELEASE "-DNDEBUG ${OPT_FLAGS_RELEASE}")

include_directories(include)

add_subdirectory(src)
