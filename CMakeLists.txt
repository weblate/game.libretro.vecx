cmake_minimum_required(VERSION 3.1)
project(game.libretro.vecx)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(VECX_LIB NAMES vecx_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(VECX_CUSTOM_BINARY ${VECX_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} VECX "")

include(CPack)
