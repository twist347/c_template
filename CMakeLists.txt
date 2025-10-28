cmake_minimum_required(VERSION 3.20)

set(T c_template)

project(${T} LANGUAGES C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)
#set(CMAKE_C_EXTENSIONS OFF)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)
set(SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)

add_executable(
        ${T}
        ${SOURCE_DIR}/example.c
        main.c)
target_include_directories(${T} PRIVATE ${INCLUDE_DIR})
target_link_libraries(${T} PRIVATE m)
target_compile_options(${T} PRIVATE -Wall -Wextra -Wpedantic)
