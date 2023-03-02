# cmake_minimum_required(VERSION 2.8)
cmake_minimum_required(VERSION 3.16)

project(DevOpsCpp)

include(CTest)
enable_testing()

add_executable(DevOpsCpp main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

install(TARGETS DevOpsCpp RUNTIME DESTINATION ${CMAKE_INSTALL_PREFIX})