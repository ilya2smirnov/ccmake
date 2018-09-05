cmake_minimum_required(VERSION 3.10)
project(test1)

add_definitions(-std=c++17)

include_directories(include)

set(MAIN_SOURCE_DIR source/${PROJECT_NAME})
set(TEST_SOURCE_DIR tests/${PROJECT_NAME})

set(COMMON_SOURCES
    ${MAIN_SOURCE_DIR}/Test1.cpp
    ${MAIN_SOURCE_DIR}/Test2.cpp)

set(MAIN_SOURCES
    ${MAIN_SOURCE_DIR}/main.cpp)

set(TEST_SOURCES
    ${TEST_SOURCE_DIR}/main_test.cpp)

add_executable(bb ${COMMON_SOURCES} ${TEST_SOURCES})
add_executable(aa ${COMMON_SOURCES} ${MAIN_SOURCES})
