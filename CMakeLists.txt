cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

project(ParaCL)

option(PARACL_BUILD_TESTS "Configure Tests target" ON)
option(PARACL_BUILD_DEMO "Configure Demo target" ON)

# PARACL project directory
set(PARACL_ROOT ${CMAKE_CURRENT_LIST_DIR})

if(PARACL_BUILD_TESTS)
  add_subdirectory(src/applications/tests)
endif()

if(PARACL_BUILD_DEMO)
  add_subdirectory(src/applications/demo)
endif()