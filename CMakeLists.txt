cmake_minimum_required(VERSION 3.0.0)
project(C++20_Features_Testing VERSION 0.1.0)

include(CTest)
enable_testing()

file(GLOB SRC CONFIGURE_DEPENDS "*.hpp" "*.cpp")
add_executable(C++20_Features_Testing ${SRC})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

target_compile_options(C++20_Features_Testing PRIVATE -std=c++20)